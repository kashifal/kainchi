<template>
  <div>
        {/* Notification Card */}
        <div className="relative w-full max-w-sm p-4 bg-white rounded-2xl shadow-lg">
          {/* Icon */}
          <div className="flex items-center">
            <div className="w-8 h-8 flex items-center justify-center bg-purple-100 text-purple-600 rounded-full">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" strokeWidth={2} stroke="currentColor" className="w-5 h-5">
                <path strokeLinecap="round" strokeLinejoin="round" d="M13.875 18.825a4.5 4.5 0 01-7.5 0M14.1 8.237a4.5 4.5 0 10-6.1 6.1M20.33 17.33a4.5 4.5 0 01-4.5-4.5M8.567 5.567a4.5 4.5 0 015.1-1.33" />
              </svg>
            </div>
            <h3 className="ml-3 text-lg font-semibold text-gray-800">Notifications</h3>
          </div>
          {/* Close Button */}
          <button className="absolute top-3 right-3 text-gray-400 hover:text-gray-600">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" strokeWidth={2} stroke="currentColor" className="w-5 h-5">
              <path strokeLinecap="round" strokeLinejoin="round" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
          {/* Text */}
          <p className="mt-3 text-sm text-gray-600 leading-relaxed">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque pretium mauris lectus, ac mattis eros pulvinar a. Donec ac.
          </p>
        </div>
        {/* Notification Card */}
        <div className="relative mt-6 w-full max-w-sm p-4 bg-white rounded-2xl shadow-lg">
          {/* Header */}
          <div className="flex items-center">
            <div className="w-8 h-8 flex items-center justify-center bg-purple-100 text-purple-600 rounded-full">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" strokeWidth={2} stroke="currentColor" className="w-5 h-5">
                <path strokeLinecap="round" strokeLinejoin="round" d="M13.875 18.825a4.5 4.5 0 01-7.5 0M14.1 8.237a4.5 4.5 0 10-6.1 6.1M20.33 17.33a4.5 4.5 0 01-4.5-4.5M8.567 5.567a4.5 4.5 0 015.1-1.33" />
              </svg>
            </div>
            <h3 className="ml-3 text-lg font-semibold text-gray-800">Message</h3>
          </div>
          {/* Close Button */}
          <button className="absolute top-3 right-3 text-gray-400 hover:text-gray-600">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" strokeWidth={2} stroke="currentColor" className="w-5 h-5">
              <path strokeLinecap="round" strokeLinejoin="round" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
          {/* Text */}
          <p className="mt-3 text-sm text-gray-600 leading-relaxed">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi quis elit non velit fringilla. Morbi quis elit non velit fringilla.
          </p>
          {/* Step Indicator */}
          <div className="mt-4 flex items-center  justify-between">
            <div className="flex items-center">
              <span className="text-xs font-medium text-gray-500 mr-2">Step 1</span>
              {/* Dots */}
              <div className="flex  items-center space-x-1">
                <span className="w-2 h-2 bg-purple-600 rounded-full" />
                <span className="w-2 h-2 bg-purple-200 rounded-full" />
                <span className="w-2 h-2 bg-purple-200 rounded-full" />
                <span className="w-2 h-2 bg-purple-200 rounded-full" />
              </div>
            </div>
            {/* Next Button */}
            <button className="px-4 py-2 text-white bg-purple-600 rounded-lg text-sm font-medium hover:bg-purple-700">
              Next
            </button>
          </div>
        </div>
      </div>
      <div className="w-80 bg-gray-100 rounded-3xl shadow-lg p-4">
        {/* Notifications Header */}
        <h2 className="text-lg font-semibold py-3 bg-white   -mt-4 w-[112%] -ml-4 shadow-2xl shadow-neutral-300 text-center p-2 rounded-full text-gray-800 mb-4">Notifications</h2>
        {/* Notification Items */}
        <div className="space-y-4">
          {/* Notification Item */}
          <div className="flex items-center">
            <img src="https://clipground.com/images/licking-ice-cream-clipart-6.jpg" alt="User" className="w-10 object-cover h-10 rounded-full mr-4" />
            <div>
              <p className="text-sm text-gray-800">
                <span className="font-semibold">David Lee</span> sent you a message.
              </p>
              <p className="text-xs text-gray-500">4 min ago</p>
            </div>
          </div>
          <div className="flex items-center">
            <img src="https://th.bing.com/th/id/OIP.28woZ3gvcoHpZ9LnQHBghAHaPL?w=976&h=2000&rs=1&pid=ImgDetMain" alt="User" className="w-10 object-cover h-10 rounded-full mr-4" />
            <div>
              <p className="text-sm text-gray-800">
                <span className="font-semibold">Alex Johnson</span> sent you a message.
              </p>
              <p className="text-xs text-gray-500">4 min ago</p>
            </div>
          </div>
          <div className="flex items-center">
            <img src="https://th.bing.com/th/id/OIP.aDEQtGy5KZ6aP8awDOsOLAHaUK?w=705&h=1920&rs=1&pid=ImgDetMain" alt="User" className="w-10 object-cover h-10 rounded-full mr-4" />
            <div>
              <p className="text-sm text-gray-800">
                <span className="font-semibold">Jonathan Chen</span> sent you mail.
              </p>
              <p className="text-xs text-gray-500">4 min ago</p>
            </div>
          </div>
          <div className="flex items-center">
            <img src="https://img.freepik.com/premium-vector/cute-little-boy-with-ice-cream_50699-459.jpg?w=1380" alt="User" className="w-10 object-cover h-10 rounded-full mr-4" />
            <div>
              <p className="text-sm text-gray-800">
                <span className="font-semibold">Robert Grant</span> sent you mail.
              </p>
              <p className="text-xs text-gray-500">4 min ago</p>
            </div>
          </div>
          <div className="flex items-center">
            <img src="https://th.bing.com/th/id/OIP.ZxSGFd93977Sp3ffSSwkJAAAAA?w=474&h=798&rs=1&pid=ImgDetMain" alt="User" className="w-10 object-cover h-10 rounded-full mr-4" />
            <div>
              <p className="text-sm text-gray-800">
                <span className="font-semibold">David James</span> sent you mail.
              </p>
              <p className="text-xs text-gray-500">4 min ago</p>
            </div>
          </div>
        </div>
        {/* View All Link */}
        <div className="mt-4 text-center">
          <a href="#" className="text-sm text-indigo-600 hover:underline">View all notifications</a>
        </div>
      </div>
</template>

<script>

</script>
