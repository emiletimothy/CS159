    r = 10*np.random.random()
    original_values = [np.sin(r),
                      np.cos(r),
                      np.tan(r),
                      np.exp(r),
                      np.sinh(r),
                      np.cosh(r),
                      np.tanh(r),
                      np.log(r+2),
                      1/np.sin(r),
                      1/np.cos(r),
                      1/np.tan(r),
                      1/np.sinh(r),
                      1/np.cosh(r),
                      1/np.tanh(r),
                      2*(r**3)+5*(r**2)+4*r,
                      2*np.sin(r) + 7*r - 4*np.log10(r+2),
                      r,
                      r**2,
                      r+np.sin(r)*np.cos(r)*np.tan(r),
                      r*np.sin(r)]
    errors = [np.random.normal(0.2, 2*np.random.random()) for i in range(20)]
    entry = [original_values[i]+errors[i] for i in range(20)]
    for error in errors:
      entry.append(np.abs(error))
    y = class_number
    dataset.append([entry, y])
