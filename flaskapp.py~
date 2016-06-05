from flask import Flask
from collections import Counter
app = Flask(__name__)

@app.route('/')
def hello_world():
	return 'Hello from Flask!'

@app.route('/post/<int:post_id>')
def show_post(post_id):
	# show the post with the given id, the id is an integer
	hr = '%d' % post_id
	with open('/hr/hr.txt', 'w') as f:
		if post_id < 100:
			f.write(hr + ' ')
		else:
			f.write(hr)
	return '%d' % post_id

@app.route('/get_hr')
def get_hr():
	ret_str = ""
	txt = open('/hr/hr.txt', 'r')
	ret_str = txt.read()
	txt.close()
	return ret_str

if __name__ == '__main__':
	app.run()
