---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075932"
---
# <span data-ttu-id="553b7-101">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="553b7-101">New-AzureCertificateSetting</span></span>

## <span data-ttu-id="553b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="553b7-102">SYNOPSIS</span></span>
<span data-ttu-id="553b7-103">Создание объекта параметров сертификата для сертификата — служба.</span><span class="sxs-lookup"><span data-stu-id="553b7-103">Creates a certificate setting object for a certificate is in a service.</span></span>

## <span data-ttu-id="553b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="553b7-104">SYNTAX</span></span>

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="553b7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="553b7-105">DESCRIPTION</span></span>
<span data-ttu-id="553b7-106">Командлет **New-AzureCertificateSetting** создает объект параметра сертификата для сертификата, который находится в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="553b7-106">The **New-AzureCertificateSetting** cmdlet creates a certificate setting object for a certificate that is in an Azure service.</span></span>

<span data-ttu-id="553b7-107">Вы можете использовать объект параметров сертификата для создания объекта конфигурации с помощью командлета **Add-AzureProvisioningConfig** .</span><span class="sxs-lookup"><span data-stu-id="553b7-107">You can use a certificate setting object to create a configuration object by using the **Add-AzureProvisioningConfig** cmdlet.</span></span>
<span data-ttu-id="553b7-108">Используйте объект конфигурации для создания виртуальной машины с помощью командлета **New-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="553b7-108">Use a configuration object to create virtual machine by using the **New-AzureVM** cmdlet.</span></span>
<span data-ttu-id="553b7-109">Вы можете использовать объект параметров сертификата для создания виртуальной машины с помощью командлета **New-AzureQuickVM** .</span><span class="sxs-lookup"><span data-stu-id="553b7-109">You can use a certificate setting object to create a virtual machine by using the **New-AzureQuickVM** cmdlet.</span></span>

## <span data-ttu-id="553b7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="553b7-110">EXAMPLES</span></span>

### <span data-ttu-id="553b7-111">Пример 1: создание объекта параметров сертификата</span><span class="sxs-lookup"><span data-stu-id="553b7-111">Example 1: Create a certificate setting object</span></span>
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

<span data-ttu-id="553b7-112">Эта команда создает объект параметра сертификата для существующего сертификата.</span><span class="sxs-lookup"><span data-stu-id="553b7-112">This command creates a certificate setting object for an existing certificate.</span></span>

### <span data-ttu-id="553b7-113">Пример 2: создание виртуальной машины, использующей объект параметров конфигурации</span><span class="sxs-lookup"><span data-stu-id="553b7-113">Example 2: Create a virtual machine that uses a configuration setting object</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="553b7-114">Первая команда добавляет сертификат ContosoCert. cer в службу с именем ContosoService с помощью командлета **Add-AzureCertificate** .</span><span class="sxs-lookup"><span data-stu-id="553b7-114">The first command adds the certificate ContosoCert.cer to the service named ContosoService by using the **Add-AzureCertificate** cmdlet.</span></span>

<span data-ttu-id="553b7-115">Вторая команда создает объект параметра сертификата и сохраняет его в переменной $CertificateSetting.</span><span class="sxs-lookup"><span data-stu-id="553b7-115">The second command creates a certificate setting object, and then stores it in the $CertificateSetting variable.</span></span>

<span data-ttu-id="553b7-116">Третья команда получает изображение из репозитория изображений с помощью командлета **Get-AzureVMImage** .</span><span class="sxs-lookup"><span data-stu-id="553b7-116">The third command gets an image from the image repository by using the **Get-AzureVMImage** cmdlet.</span></span>
<span data-ttu-id="553b7-117">Эта команда хранит изображение в переменной $Image.</span><span class="sxs-lookup"><span data-stu-id="553b7-117">This command store the image in the $Image variable.</span></span>

<span data-ttu-id="553b7-118">Последняя команда создает объект конфигурации виртуальной машины на основе изображения в $Image с помощью командлета **New-AzureVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="553b7-118">The final command creates a virtual machine configuration object based on the image in $Image by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="553b7-119">Команда передает этот объект командлету **Add-AzureProvisioningConfig** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="553b7-119">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="553b7-120">Этот командлет добавляет данные подготовки в конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="553b7-120">That cmdlet add provisioning information to the configuration.</span></span>
<span data-ttu-id="553b7-121">Команда передает объект в командлет **New-AzureVM** , который создает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="553b7-121">The command passes the object to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

## <span data-ttu-id="553b7-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="553b7-122">PARAMETERS</span></span>

### <span data-ttu-id="553b7-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="553b7-123">-InformationAction</span></span>
<span data-ttu-id="553b7-124">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="553b7-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="553b7-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="553b7-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="553b7-126">Продолжал</span><span class="sxs-lookup"><span data-stu-id="553b7-126">Continue</span></span>
- <span data-ttu-id="553b7-127">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="553b7-127">Ignore</span></span>
- <span data-ttu-id="553b7-128">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="553b7-128">Inquire</span></span>
- <span data-ttu-id="553b7-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="553b7-129">SilentlyContinue</span></span>
- <span data-ttu-id="553b7-130">Остановить</span><span class="sxs-lookup"><span data-stu-id="553b7-130">Stop</span></span>
- <span data-ttu-id="553b7-131">Рвать</span><span class="sxs-lookup"><span data-stu-id="553b7-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="553b7-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="553b7-132">-InformationVariable</span></span>
<span data-ttu-id="553b7-133">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="553b7-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="553b7-134">-Столбец StoreName</span><span class="sxs-lookup"><span data-stu-id="553b7-134">-StoreName</span></span>
<span data-ttu-id="553b7-135">Указывает хранилище сертификатов, в которое нужно добавить сертификат.</span><span class="sxs-lookup"><span data-stu-id="553b7-135">Specifies the certificate store in which to put the certificate.</span></span>
<span data-ttu-id="553b7-136">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="553b7-136">Valid values are:</span></span> 

- <span data-ttu-id="553b7-137">AddressBook</span><span class="sxs-lookup"><span data-stu-id="553b7-137">AddressBook</span></span>
- <span data-ttu-id="553b7-138">AuthRoot</span><span class="sxs-lookup"><span data-stu-id="553b7-138">AuthRoot</span></span>
- <span data-ttu-id="553b7-139">CertificateAuthority</span><span class="sxs-lookup"><span data-stu-id="553b7-139">CertificateAuthority</span></span>
- <span data-ttu-id="553b7-140">Запрещены</span><span class="sxs-lookup"><span data-stu-id="553b7-140">Disallowed</span></span>
- <span data-ttu-id="553b7-141">Настроек</span><span class="sxs-lookup"><span data-stu-id="553b7-141">My</span></span>
- <span data-ttu-id="553b7-142">Узла</span><span class="sxs-lookup"><span data-stu-id="553b7-142">Root</span></span>
- <span data-ttu-id="553b7-143">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="553b7-143">TrustedPeople</span></span>
- <span data-ttu-id="553b7-144">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="553b7-144">TrustedPublisher</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="553b7-145">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="553b7-145">-Thumbprint</span></span>
<span data-ttu-id="553b7-146">Указывает отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="553b7-146">Specifies the thumbprint of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="553b7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="553b7-147">CommonParameters</span></span>
<span data-ttu-id="553b7-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="553b7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="553b7-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="553b7-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="553b7-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="553b7-150">INPUTS</span></span>

## <span data-ttu-id="553b7-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="553b7-151">OUTPUTS</span></span>

## <span data-ttu-id="553b7-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="553b7-152">NOTES</span></span>

## <span data-ttu-id="553b7-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="553b7-153">RELATED LINKS</span></span>

[<span data-ttu-id="553b7-154">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="553b7-154">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="553b7-155">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="553b7-155">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="553b7-156">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="553b7-156">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="553b7-157">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="553b7-157">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="553b7-158">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="553b7-158">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)

[<span data-ttu-id="553b7-159">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="553b7-159">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="553b7-160">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="553b7-160">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


