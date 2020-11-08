---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 19A87B24-C5A6-4505-BB54-973B24BCC68E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 821927fc465ed5af048a2f27ed84da8c12b9caa5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076536"
---
# <span data-ttu-id="9b2d8-101">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="9b2d8-101">Get-AzureVMDscExtensionStatus</span></span>

## <span data-ttu-id="9b2d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b2d8-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2d8-103">Получает состояние расширения DSC для всех виртуальных машин, развернутых в облачной службе или для определенной виртуальной машины в службе.</span><span class="sxs-lookup"><span data-stu-id="9b2d8-103">Gets the DSC extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="9b2d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b2d8-104">SYNTAX</span></span>

### <span data-ttu-id="9b2d8-105">GetStatusByServiceAndVMName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9b2d8-105">GetStatusByServiceAndVMName (Default)</span></span>
```
Get-AzureVMDscExtensionStatus [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9b2d8-106">GetStatusByVM</span><span class="sxs-lookup"><span data-stu-id="9b2d8-106">GetStatusByVM</span></span>
```
Get-AzureVMDscExtensionStatus -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9b2d8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b2d8-107">DESCRIPTION</span></span>
<span data-ttu-id="9b2d8-108">Командлет **Get-AzureVMDscExtensionStatus** получает состояние расширения нужной конфигурации (DSC) для всех виртуальных машин, развернутых в облачной службе или для определенной виртуальной машины в службе.</span><span class="sxs-lookup"><span data-stu-id="9b2d8-108">The **Get-AzureVMDscExtensionStatus** cmdlet gets the Desired State Configuration (DSC) extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="9b2d8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b2d8-109">EXAMPLES</span></span>

### <span data-ttu-id="9b2d8-110">1:</span><span class="sxs-lookup"><span data-stu-id="9b2d8-110">1:</span></span>
```

```

## <span data-ttu-id="9b2d8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b2d8-111">PARAMETERS</span></span>

### <span data-ttu-id="9b2d8-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9b2d8-112">-InformationAction</span></span>
<span data-ttu-id="9b2d8-113">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="9b2d8-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9b2d8-114">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9b2d8-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9b2d8-115">Продолжал</span><span class="sxs-lookup"><span data-stu-id="9b2d8-115">Continue</span></span>
- <span data-ttu-id="9b2d8-116">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="9b2d8-116">Ignore</span></span>
- <span data-ttu-id="9b2d8-117">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="9b2d8-117">Inquire</span></span>
- <span data-ttu-id="9b2d8-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9b2d8-118">SilentlyContinue</span></span>
- <span data-ttu-id="9b2d8-119">Остановить</span><span class="sxs-lookup"><span data-stu-id="9b2d8-119">Stop</span></span>
- <span data-ttu-id="9b2d8-120">Рвать</span><span class="sxs-lookup"><span data-stu-id="9b2d8-120">Suspend</span></span>

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

### <span data-ttu-id="9b2d8-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9b2d8-121">-InformationVariable</span></span>
<span data-ttu-id="9b2d8-122">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="9b2d8-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9b2d8-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9b2d8-123">-Name</span></span>
<span data-ttu-id="9b2d8-124">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9b2d8-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b2d8-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="9b2d8-125">-Profile</span></span>
<span data-ttu-id="9b2d8-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9b2d8-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9b2d8-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9b2d8-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9b2d8-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9b2d8-128">-ServiceName</span></span>
<span data-ttu-id="9b2d8-129">Указывает имя службы.</span><span class="sxs-lookup"><span data-stu-id="9b2d8-129">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b2d8-130">-VM</span><span class="sxs-lookup"><span data-stu-id="9b2d8-130">-VM</span></span>
<span data-ttu-id="9b2d8-131">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9b2d8-131">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: GetStatusByVM
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b2d8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b2d8-132">CommonParameters</span></span>
<span data-ttu-id="9b2d8-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b2d8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b2d8-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b2d8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b2d8-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b2d8-135">INPUTS</span></span>

## <span data-ttu-id="9b2d8-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b2d8-136">OUTPUTS</span></span>

### <span data-ttu-id="9b2d8-137">Microsoft. WindowsAzure. Commands. ServiceManagement. IaaS. Extensions. VirtualMachineDscExtensionStatusContext</span><span class="sxs-lookup"><span data-stu-id="9b2d8-137">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionStatusContext</span></span>

## <span data-ttu-id="9b2d8-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b2d8-138">NOTES</span></span>

## <span data-ttu-id="9b2d8-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b2d8-139">RELATED LINKS</span></span>

[<span data-ttu-id="9b2d8-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9b2d8-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="9b2d8-141">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9b2d8-141">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="9b2d8-142">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9b2d8-142">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


