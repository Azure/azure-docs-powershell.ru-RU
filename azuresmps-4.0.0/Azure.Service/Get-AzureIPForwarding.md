---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BE661AC7-BA39-4D6A-8083-16CE9327DC08
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4c84155484435a9601af005393593040c9cfe4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076348"
---
# <span data-ttu-id="7aa8e-101">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="7aa8e-101">Get-AzureIPForwarding</span></span>

## <span data-ttu-id="7aa8e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7aa8e-102">SYNOPSIS</span></span>
<span data-ttu-id="7aa8e-103">Возвращает состояние пересылки IP.</span><span class="sxs-lookup"><span data-stu-id="7aa8e-103">Gets the status of IP forwarding.</span></span>

## <span data-ttu-id="7aa8e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7aa8e-104">SYNTAX</span></span>

### <span data-ttu-id="7aa8e-105">IaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="7aa8e-105">IaaSIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7aa8e-106">SlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="7aa8e-106">SlotIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7aa8e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7aa8e-107">DESCRIPTION</span></span>
<span data-ttu-id="7aa8e-108">Командлет **Get-AzureIPForwarding** возвращает состояние IP-переадресации.</span><span class="sxs-lookup"><span data-stu-id="7aa8e-108">The **Get-AzureIPForwarding** cmdlet gets the status of IP forwarding.</span></span>

## <span data-ttu-id="7aa8e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7aa8e-109">EXAMPLES</span></span>

### <span data-ttu-id="7aa8e-110">Пример 1: получение состояния IP-переадресации для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="7aa8e-110">Example 1: Get IP forwarding status for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureIPForwarding
Disabled
```

<span data-ttu-id="7aa8e-111">Эта команда получает виртуальную машину с именем ContosoVM06 для службы с именем ContosoService и передает этот объект виртуальной машины в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="7aa8e-111">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="7aa8e-112">Текущий командлет получает состояние IP-переадресации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7aa8e-112">The current cmdlet gets the status of IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="7aa8e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7aa8e-113">PARAMETERS</span></span>

### <span data-ttu-id="7aa8e-114">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="7aa8e-114">-NetworkInterfaceName</span></span>
<span data-ttu-id="7aa8e-115">Указывает имя сетевого адаптера, для которого этот командлет получает IP-состояние пересылки.</span><span class="sxs-lookup"><span data-stu-id="7aa8e-115">Specifies the name of the network adapter for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aa8e-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="7aa8e-116">-Profile</span></span>
<span data-ttu-id="7aa8e-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7aa8e-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7aa8e-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7aa8e-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7aa8e-119">-RoleName</span><span class="sxs-lookup"><span data-stu-id="7aa8e-119">-RoleName</span></span>
<span data-ttu-id="7aa8e-120">Указывает имя роли PaaS, для которой этот командлет получает IP-состояние пересылки.</span><span class="sxs-lookup"><span data-stu-id="7aa8e-120">Specifies the name of a PaaS role for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aa8e-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7aa8e-121">-ServiceName</span></span>
<span data-ttu-id="7aa8e-122">Указывает имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="7aa8e-122">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="7aa8e-123">Роль PaaS принадлежит службе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="7aa8e-123">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aa8e-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="7aa8e-124">-Slot</span></span>
<span data-ttu-id="7aa8e-125">Указывает гнездо PaaS.</span><span class="sxs-lookup"><span data-stu-id="7aa8e-125">Specifies a PaaS slot.</span></span>
<span data-ttu-id="7aa8e-126">Роль PaaS, для которой этот командлет получает состояние переадресации, имеет ячейку, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="7aa8e-126">The PaaS role for which this cmdlet gets forwarding status has the slot that this parameter specifies.</span></span>
<span data-ttu-id="7aa8e-127">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="7aa8e-127">Valid values are:</span></span> 

- <span data-ttu-id="7aa8e-128">Спецификации</span><span class="sxs-lookup"><span data-stu-id="7aa8e-128">Production</span></span>
- <span data-ttu-id="7aa8e-129">Промежуточного хранения</span><span class="sxs-lookup"><span data-stu-id="7aa8e-129">Staging</span></span> 

<span data-ttu-id="7aa8e-130">Значением по умолчанию является "производство".</span><span class="sxs-lookup"><span data-stu-id="7aa8e-130">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa8e-131">-VM</span><span class="sxs-lookup"><span data-stu-id="7aa8e-131">-VM</span></span>
<span data-ttu-id="7aa8e-132">Указывает объект виртуальной машины, для которого этот командлет получает IP-состояние пересылки.</span><span class="sxs-lookup"><span data-stu-id="7aa8e-132">Specifies the virtual machine object for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7aa8e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aa8e-133">CommonParameters</span></span>
<span data-ttu-id="7aa8e-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7aa8e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aa8e-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aa8e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aa8e-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7aa8e-136">INPUTS</span></span>

## <span data-ttu-id="7aa8e-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7aa8e-137">OUTPUTS</span></span>

### <span data-ttu-id="7aa8e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7aa8e-138">System.String</span></span>

## <span data-ttu-id="7aa8e-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="7aa8e-139">NOTES</span></span>

## <span data-ttu-id="7aa8e-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7aa8e-140">RELATED LINKS</span></span>

[<span data-ttu-id="7aa8e-141">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="7aa8e-141">Set-AzureIPForwarding</span></span>](./Set-AzureIPForwarding.md)


