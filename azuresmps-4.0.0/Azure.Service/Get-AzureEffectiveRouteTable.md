---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 82CF6E71-FFE2-4B2C-8AAD-04C137AD5706
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49f9cce74cb2621d6c9ff51485b7c4bce4a302bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076353"
---
# <span data-ttu-id="17b00-101">Get-AzureEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="17b00-101">Get-AzureEffectiveRouteTable</span></span>

## <span data-ttu-id="17b00-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17b00-102">SYNOPSIS</span></span>
<span data-ttu-id="17b00-103">Возвращает маршрут, примененный к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="17b00-103">Gets the route applied in a virtual machine.</span></span>

## <span data-ttu-id="17b00-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17b00-104">SYNTAX</span></span>

### <span data-ttu-id="17b00-105">IaaSGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="17b00-105">IaaSGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="17b00-106">SlotGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="17b00-106">SlotGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -ServiceName <String> [-Slot <String>] -RoleInstanceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="17b00-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17b00-107">DESCRIPTION</span></span>
<span data-ttu-id="17b00-108">Командлет **Get-AzureEffectiveRouteTable** получает маршрут, примененный к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="17b00-108">The **Get-AzureEffectiveRouteTable** cmdlet gets the route applied in a virtual machine.</span></span>
<span data-ttu-id="17b00-109">Для завершения этой операции может потребоваться несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="17b00-109">This operation could take several seconds to finish.</span></span>

## <span data-ttu-id="17b00-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17b00-110">EXAMPLES</span></span>

### <span data-ttu-id="17b00-111">Пример 1: получение действующего маршрута, примененного к виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="17b00-111">Example 1: Get the effective route applied a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureEffectiveRouteTable
```

<span data-ttu-id="17b00-112">Эта команда получает виртуальную машину с именем ContosoVM06 для службы с именем ContosoService и передает этот объект виртуальной машины в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="17b00-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="17b00-113">Текущий командлет получает маршрут, примененный к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="17b00-113">The current cmdlet gets the route applied to that virtual machine.</span></span>

## <span data-ttu-id="17b00-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17b00-114">PARAMETERS</span></span>

### <span data-ttu-id="17b00-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="17b00-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="17b00-116">Указывает имя сетевого адаптера, для которого этот командлет получает действующие маршруты.</span><span class="sxs-lookup"><span data-stu-id="17b00-116">Specifies the name of the network adapter for which this cmdlet gets effective routes.</span></span>

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

### <span data-ttu-id="17b00-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="17b00-117">-Profile</span></span>
<span data-ttu-id="17b00-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="17b00-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="17b00-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="17b00-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="17b00-120">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="17b00-120">-RoleInstanceName</span></span>
<span data-ttu-id="17b00-121">Указывает имя роли PaaS, для которой этот командлет получает действующие маршруты.</span><span class="sxs-lookup"><span data-stu-id="17b00-121">Specifies the name of a PaaS role for which this cmdlet gets effective routes.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17b00-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="17b00-122">-ServiceName</span></span>
<span data-ttu-id="17b00-123">Указывает имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="17b00-123">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="17b00-124">Роль PaaS, для которой этот командлет получает действующие маршруты, относятся к службе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="17b00-124">The PaaS role for which this cmdlet gets effective routes belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="17b00-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="17b00-125">-Slot</span></span>
<span data-ttu-id="17b00-126">Указывает гнездо PaaS.</span><span class="sxs-lookup"><span data-stu-id="17b00-126">Specifies a PaaS slot.</span></span>
<span data-ttu-id="17b00-127">Роль PaaS, для которой этот командлет получает действующие маршруты, имеет ячейку, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="17b00-127">The PaaS role for which this cmdlet gets effective routes has the slot that this parameter specifies.</span></span>
<span data-ttu-id="17b00-128">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="17b00-128">Valid values are:</span></span> 

- <span data-ttu-id="17b00-129">Спецификации</span><span class="sxs-lookup"><span data-stu-id="17b00-129">Production</span></span>
- <span data-ttu-id="17b00-130">Промежуточного хранения</span><span class="sxs-lookup"><span data-stu-id="17b00-130">Staging</span></span> 

<span data-ttu-id="17b00-131">Значением по умолчанию является "производство".</span><span class="sxs-lookup"><span data-stu-id="17b00-131">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b00-132">-VM</span><span class="sxs-lookup"><span data-stu-id="17b00-132">-VM</span></span>
<span data-ttu-id="17b00-133">Указывает объект виртуальной машины, для которого этот командлет получает действующие маршруты.</span><span class="sxs-lookup"><span data-stu-id="17b00-133">Specifies the virtual machine object for which this cmdlet gets effective routes.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17b00-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b00-134">CommonParameters</span></span>
<span data-ttu-id="17b00-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17b00-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b00-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17b00-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b00-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17b00-137">INPUTS</span></span>

## <span data-ttu-id="17b00-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17b00-138">OUTPUTS</span></span>

### <span data-ttu-id="17b00-139">System. Collections. Generic. IEnumerable<Microsoft. EffectiveRouteTable. Management. Networking., Microsoft. WindowsAzure. Management. Network></span><span class="sxs-lookup"><span data-stu-id="17b00-139">System.Collections.Generic.IEnumerable<Microsoft.WindowsAzure.Management.Network.Models.EffectiveRouteTable, Microsoft.WindowsAzure.Management.Network></span></span>

## <span data-ttu-id="17b00-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="17b00-140">NOTES</span></span>

## <span data-ttu-id="17b00-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17b00-141">RELATED LINKS</span></span>

[<span data-ttu-id="17b00-142">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="17b00-142">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="17b00-143">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="17b00-143">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="17b00-144">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="17b00-144">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)

[<span data-ttu-id="17b00-145">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="17b00-145">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="17b00-146">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="17b00-146">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


