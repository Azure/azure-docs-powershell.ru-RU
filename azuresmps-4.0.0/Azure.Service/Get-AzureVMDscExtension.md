---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9D6D1890-9442-45F1-A3AA-BB1DB5CB33D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 462d40e463edf6894810ac6e00e39b9c7a9eabe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076538"
---
# <span data-ttu-id="5ee0a-101">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="5ee0a-101">Get-AzureVMDscExtension</span></span>

## <span data-ttu-id="5ee0a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ee0a-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee0a-103">Получает параметры расширения DSC на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5ee0a-103">Gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="5ee0a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ee0a-104">SYNTAX</span></span>

```
Get-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5ee0a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ee0a-105">DESCRIPTION</span></span>
<span data-ttu-id="5ee0a-106">Командлет **Get-AzureVMDscExtension** получает параметры расширения DSC на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5ee0a-106">The **Get-AzureVMDscExtension** cmdlet gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="5ee0a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ee0a-107">EXAMPLES</span></span>

### <span data-ttu-id="5ee0a-108">Пример 1: получение значения расширения DSC на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="5ee0a-108">Example 1: Get the setting of the DSC Extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMDscExtension -VM $VMModulesUrl
https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zipConfigurationFunction : MyConfiguration.ps1\MyConfigurationProperties            : {ServerName}ExtensionName         : DSCPublisher             : Microsoft.PowershellVersion               : 1.*PrivateConfiguration  :PublicConfiguration   : {"ModulesUrl": "https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zip","ConfigurationFunction": "MyConfiguration.ps1\\MyConfiguration","Properties": {"ServerName": "C:\\MyDirectory"}}ReferenceName         : DSCState                 : EnableRoleName              : my-vm
```

<span data-ttu-id="5ee0a-109">Эта команда получает параметры расширения DSC на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5ee0a-109">This command gets the settings of the DSC Extension on a virtual machine.</span></span>

## <span data-ttu-id="5ee0a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ee0a-110">PARAMETERS</span></span>

### <span data-ttu-id="5ee0a-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5ee0a-111">-InformationAction</span></span>
<span data-ttu-id="5ee0a-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="5ee0a-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5ee0a-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5ee0a-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5ee0a-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="5ee0a-114">Continue</span></span>
- <span data-ttu-id="5ee0a-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="5ee0a-115">Ignore</span></span>
- <span data-ttu-id="5ee0a-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="5ee0a-116">Inquire</span></span>
- <span data-ttu-id="5ee0a-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5ee0a-117">SilentlyContinue</span></span>
- <span data-ttu-id="5ee0a-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="5ee0a-118">Stop</span></span>
- <span data-ttu-id="5ee0a-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="5ee0a-119">Suspend</span></span>

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

### <span data-ttu-id="5ee0a-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5ee0a-120">-InformationVariable</span></span>
<span data-ttu-id="5ee0a-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="5ee0a-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5ee0a-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="5ee0a-122">-Profile</span></span>
<span data-ttu-id="5ee0a-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5ee0a-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5ee0a-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5ee0a-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5ee0a-125">-VM</span><span class="sxs-lookup"><span data-stu-id="5ee0a-125">-VM</span></span>
<span data-ttu-id="5ee0a-126">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5ee0a-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="5ee0a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee0a-127">CommonParameters</span></span>
<span data-ttu-id="5ee0a-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ee0a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee0a-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ee0a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee0a-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ee0a-130">INPUTS</span></span>

## <span data-ttu-id="5ee0a-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ee0a-131">OUTPUTS</span></span>

### <span data-ttu-id="5ee0a-132">Microsoft. WindowsAzure. Commands. ServiceManagement. IaaS. Extensions. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="5ee0a-132">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="5ee0a-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ee0a-133">NOTES</span></span>

## <span data-ttu-id="5ee0a-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ee0a-134">RELATED LINKS</span></span>

[<span data-ttu-id="5ee0a-135">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="5ee0a-135">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="5ee0a-136">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="5ee0a-136">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="5ee0a-137">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="5ee0a-137">Get-AzureVMDscExtensionStatus</span></span>](./Get-AzureVMDscExtensionStatus.md)


