---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075955"
---
# <span data-ttu-id="ea27a-101">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="ea27a-101">Set-AzurePublicIP</span></span>

## <span data-ttu-id="ea27a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea27a-102">SYNOPSIS</span></span>
<span data-ttu-id="ea27a-103">Добавляет общедоступный IP-адрес виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="ea27a-103">Adds a Public IP to an Azure virtual machine.</span></span>

## <span data-ttu-id="ea27a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea27a-104">SYNTAX</span></span>

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ea27a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea27a-105">DESCRIPTION</span></span>
<span data-ttu-id="ea27a-106">Командлет **Set-AzurePublicIP** добавляет общедоступный IP-адрес виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="ea27a-106">The **Set-AzurePublicIP** cmdlet adds a Public IP to an Azure virtual machine.</span></span>
<span data-ttu-id="ea27a-107">Если вы запускаете этот командлет для существующей виртуальной машины, обновите виртуальную машину для реализации изменений.</span><span class="sxs-lookup"><span data-stu-id="ea27a-107">If you run this cmdlet for an existing virtual machine, update the virtual machine to implement your changes.</span></span>
<span data-ttu-id="ea27a-108">Вы можете указать метку доменного имени, чтобы создать соответствующую запись DNS для общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ea27a-108">You can specify a domain name label to create a corresponding DNS entry for the public IP.</span></span>

## <span data-ttu-id="ea27a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea27a-109">EXAMPLES</span></span>

### <span data-ttu-id="ea27a-110">Пример 1: Добавление общедоступного IP-адреса для существующей виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="ea27a-110">Example 1: Add a Public IP to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

<span data-ttu-id="ea27a-111">Эта команда получает виртуальную машину с именем FTPInstance в службе с именем FTPInAzure с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="ea27a-111">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="ea27a-112">Команда передает эту виртуальную машину в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="ea27a-112">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ea27a-113">Текущий командлет добавляет ftpip имя общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ea27a-113">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="ea27a-114">Команда передает виртуальную машину командлету **Update-AzureVM** , который реализует ваши изменения.</span><span class="sxs-lookup"><span data-stu-id="ea27a-114">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="ea27a-115">Пример 2: Добавление общедоступного IP-адреса для новой виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="ea27a-115">Example 2: Add a Public IP to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="ea27a-116">Эта команда создает объект конфигурации виртуальной машины с помощью командлета **New-AzureVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="ea27a-116">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="ea27a-117">Команда передает этот объект в командлет **Add-AzureProvisioningConfig** , который обеспечивает дополнительную настройку.</span><span class="sxs-lookup"><span data-stu-id="ea27a-117">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet, which provides additional configuration.</span></span>
<span data-ttu-id="ea27a-118">Текущий командлет добавляет ftpip имя общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ea27a-118">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="ea27a-119">Команда передает конфигурацию в командлет **New-AzureVM** , который создает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ea27a-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="ea27a-120">Пример 3: Добавление общедоступного IP-адреса и метки к существующей виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="ea27a-120">Example 3: Add a Public IP and label to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

<span data-ttu-id="ea27a-121">Эта команда получает виртуальную машину с именем FTPInstance в службе с именем FTPInAzure с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="ea27a-121">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="ea27a-122">Команда передает эту виртуальную машину в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="ea27a-122">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ea27a-123">Текущий командлет добавляет общедоступные IP-имена ftpip и Label ipname.</span><span class="sxs-lookup"><span data-stu-id="ea27a-123">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="ea27a-124">Эта команда обновляет виртуальную машину, которая реализует изменения.</span><span class="sxs-lookup"><span data-stu-id="ea27a-124">The command updates the virtual machine, which implements your changes.</span></span>

### <span data-ttu-id="ea27a-125">Пример 4: Добавление общедоступного IP-адреса и метки к новой виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="ea27a-125">Example 4: Add a Public IP and label to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="ea27a-126">Эта команда создает объект конфигурации виртуальной машины и передает этот объект в **Add-AzureProvisioningConfig** , который предоставляет дополнительные настройки.</span><span class="sxs-lookup"><span data-stu-id="ea27a-126">This command creates a virtual machine configuration object, and then passes that object to **Add-AzureProvisioningConfig** , which provides additional configuration.</span></span>
<span data-ttu-id="ea27a-127">Текущий командлет добавляет общедоступные IP-имена ftpip и Label ipname.</span><span class="sxs-lookup"><span data-stu-id="ea27a-127">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="ea27a-128">Команда создает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ea27a-128">The command creates the virtual machine.</span></span>

## <span data-ttu-id="ea27a-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea27a-129">PARAMETERS</span></span>

### <span data-ttu-id="ea27a-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="ea27a-130">-DomainNameLabel</span></span>
<span data-ttu-id="ea27a-131">Указывает имя, которое будет использоваться для соответствующей записи DNS для общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ea27a-131">Specifies the name to use for a corresponding DNS entry for the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea27a-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ea27a-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ea27a-133">Задает тайм-аут простоя TCP в минутах.</span><span class="sxs-lookup"><span data-stu-id="ea27a-133">Specifies the TCP idle time-out period in minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea27a-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ea27a-134">-InformationAction</span></span>
<span data-ttu-id="ea27a-135">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="ea27a-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ea27a-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ea27a-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea27a-137">Продолжал</span><span class="sxs-lookup"><span data-stu-id="ea27a-137">Continue</span></span>
- <span data-ttu-id="ea27a-138">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="ea27a-138">Ignore</span></span>
- <span data-ttu-id="ea27a-139">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="ea27a-139">Inquire</span></span>
- <span data-ttu-id="ea27a-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ea27a-140">SilentlyContinue</span></span>
- <span data-ttu-id="ea27a-141">Остановить</span><span class="sxs-lookup"><span data-stu-id="ea27a-141">Stop</span></span>
- <span data-ttu-id="ea27a-142">Рвать</span><span class="sxs-lookup"><span data-stu-id="ea27a-142">Suspend</span></span>

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

### <span data-ttu-id="ea27a-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ea27a-143">-InformationVariable</span></span>
<span data-ttu-id="ea27a-144">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="ea27a-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ea27a-145">-Profile</span><span class="sxs-lookup"><span data-stu-id="ea27a-145">-Profile</span></span>
<span data-ttu-id="ea27a-146">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ea27a-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ea27a-147">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ea27a-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea27a-148">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="ea27a-148">-PublicIPName</span></span>
<span data-ttu-id="ea27a-149">Указывает общедоступное имя IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ea27a-149">Specifies the Public IP name.</span></span>

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

### <span data-ttu-id="ea27a-150">-VM</span><span class="sxs-lookup"><span data-stu-id="ea27a-150">-VM</span></span>
<span data-ttu-id="ea27a-151">Указывает виртуальную машину, к которой этот командлет добавляет общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="ea27a-151">Specifies the virtual machine to which this cmdlet adds Public IP.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea27a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea27a-152">CommonParameters</span></span>
<span data-ttu-id="ea27a-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea27a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea27a-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea27a-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea27a-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea27a-155">INPUTS</span></span>

## <span data-ttu-id="ea27a-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea27a-156">OUTPUTS</span></span>

### <span data-ttu-id="ea27a-157">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="ea27a-157">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="ea27a-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea27a-158">NOTES</span></span>

## <span data-ttu-id="ea27a-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea27a-159">RELATED LINKS</span></span>

[<span data-ttu-id="ea27a-160">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="ea27a-160">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="ea27a-161">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ea27a-161">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="ea27a-162">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ea27a-162">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="ea27a-163">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="ea27a-163">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="ea27a-164">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="ea27a-164">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="ea27a-165">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ea27a-165">Update-AzureVM</span></span>](./Update-AzureVM.md)


