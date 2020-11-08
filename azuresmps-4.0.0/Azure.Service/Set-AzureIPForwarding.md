---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA9686AF-2D03-43DB-A91B-50D06D674A3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8da83231a16f4c846f09d03374d6e35757e1ba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075956"
---
# <span data-ttu-id="e39e6-101">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="e39e6-101">Set-AzureIPForwarding</span></span>

## <span data-ttu-id="e39e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e39e6-102">SYNOPSIS</span></span>
<span data-ttu-id="e39e6-103">Включение или отключение пересылки IP.</span><span class="sxs-lookup"><span data-stu-id="e39e6-103">Enables or disables IP forwarding.</span></span>

## <span data-ttu-id="e39e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e39e6-104">SYNTAX</span></span>

### <span data-ttu-id="e39e6-105">EnableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="e39e6-105">EnableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e39e6-106">DisableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="e39e6-106">DisableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e39e6-107">EnableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="e39e6-107">EnableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e39e6-108">DisableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="e39e6-108">DisableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e39e6-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e39e6-109">DESCRIPTION</span></span>
<span data-ttu-id="e39e6-110">Командлет **Set-AzureIPForwarding** включает или выключает IP-переадресацию для виртуальной машины, платформы в качестве роли службы (PaaS) или сетевого адаптера, который принадлежит к роли виртуальной машины или PaaS.</span><span class="sxs-lookup"><span data-stu-id="e39e6-110">The **Set-AzureIPForwarding** cmdlet enables or disables IP forwarding for a virtual machine, for a platform as a service (PaaS) role, or a network adapter that belongs to a virtual machine or PaaS role.</span></span>

## <span data-ttu-id="e39e6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e39e6-111">EXAMPLES</span></span>

### <span data-ttu-id="e39e6-112">Пример 1: включение IP-переадресации для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="e39e6-112">Example 1: Enable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Enable
```

<span data-ttu-id="e39e6-113">Эта команда получает виртуальную машину с именем ContosoVM06 для службы с именем ContosoService и передает этот объект виртуальной машины в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="e39e6-113">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="e39e6-114">Текущий командлет включает IP-переадресацию для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e39e6-114">The current cmdlet enables IP forwarding for that virtual machine.</span></span>

### <span data-ttu-id="e39e6-115">Пример 2: Отключение пересылки IP для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="e39e6-115">Example 2: Disable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Disable
```

<span data-ttu-id="e39e6-116">Эта команда получает виртуальную машину с именем ContosoVM06 для службы с именем ContosoService и передает этот объект виртуальной машины в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="e39e6-116">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="e39e6-117">Текущий командлет отключает IP-переадресацию для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e39e6-117">The current cmdlet disables IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="e39e6-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e39e6-118">PARAMETERS</span></span>

### <span data-ttu-id="e39e6-119">-Отключение</span><span class="sxs-lookup"><span data-stu-id="e39e6-119">-Disable</span></span>
<span data-ttu-id="e39e6-120">Указывает на то, что этот командлет отключает IP-переадресацию.</span><span class="sxs-lookup"><span data-stu-id="e39e6-120">Indicates that this cmdlet disables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableIaaSIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39e6-121">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="e39e6-121">-Enable</span></span>
<span data-ttu-id="e39e6-122">Указывает на то, что этот командлет включает IP-переадресацию.</span><span class="sxs-lookup"><span data-stu-id="e39e6-122">Indicates that this cmdlet enables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableIaaSIPForwardingParamSet, EnableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39e6-123">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="e39e6-123">-NetworkInterfaceName</span></span>
<span data-ttu-id="e39e6-124">Указывает имя сетевого адаптера, для которого этот командлет задает IP-переадресацию.</span><span class="sxs-lookup"><span data-stu-id="e39e6-124">Specifies the name of the network adapter on which this cmdlet sets IP forwarding.</span></span>

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

### <span data-ttu-id="e39e6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e39e6-125">-PassThru</span></span>
<span data-ttu-id="e39e6-126">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e39e6-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e39e6-127">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e39e6-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39e6-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="e39e6-128">-Profile</span></span>
<span data-ttu-id="e39e6-129">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e39e6-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e39e6-130">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e39e6-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e39e6-131">-RoleName</span><span class="sxs-lookup"><span data-stu-id="e39e6-131">-RoleName</span></span>
<span data-ttu-id="e39e6-132">Указывает имя роли PaaS, для которой этот командлет задает IP-переадресацию.</span><span class="sxs-lookup"><span data-stu-id="e39e6-132">Specifies the name of a PaaS role on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e39e6-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e39e6-133">-ServiceName</span></span>
<span data-ttu-id="e39e6-134">Указывает имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="e39e6-134">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="e39e6-135">Роль PaaS принадлежит службе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="e39e6-135">The PaaS role belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="e39e6-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="e39e6-136">-Slot</span></span>
<span data-ttu-id="e39e6-137">Указывает гнездо PaaS.</span><span class="sxs-lookup"><span data-stu-id="e39e6-137">Specifies a PaaS slot.</span></span>
<span data-ttu-id="e39e6-138">Роль PaaS, для которой этот командлет задает переадресацию, имеет ячейку, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="e39e6-138">The PaaS role for which this cmdlet sets forwarding has the slot that this parameter specifies.</span></span>
<span data-ttu-id="e39e6-139">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="e39e6-139">Valid values are:</span></span>

- <span data-ttu-id="e39e6-140">Спецификации</span><span class="sxs-lookup"><span data-stu-id="e39e6-140">Production</span></span>
- <span data-ttu-id="e39e6-141">Промежуточного хранения</span><span class="sxs-lookup"><span data-stu-id="e39e6-141">Staging</span></span>

<span data-ttu-id="e39e6-142">Значением по умолчанию является "производство".</span><span class="sxs-lookup"><span data-stu-id="e39e6-142">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e39e6-143">-VM</span><span class="sxs-lookup"><span data-stu-id="e39e6-143">-VM</span></span>
<span data-ttu-id="e39e6-144">Указывает объект виртуальной машины, для которого этот командлет задает IP-переадресацию.</span><span class="sxs-lookup"><span data-stu-id="e39e6-144">Specifies the virtual machine object on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: EnableIaaSIPForwardingParamSet, DisableIaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e39e6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e39e6-145">CommonParameters</span></span>
<span data-ttu-id="e39e6-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e39e6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e39e6-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e39e6-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e39e6-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e39e6-148">INPUTS</span></span>

## <span data-ttu-id="e39e6-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e39e6-149">OUTPUTS</span></span>

### <span data-ttu-id="e39e6-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e39e6-150">System.Boolean</span></span>

## <span data-ttu-id="e39e6-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="e39e6-151">NOTES</span></span>

## <span data-ttu-id="e39e6-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e39e6-152">RELATED LINKS</span></span>

[<span data-ttu-id="e39e6-153">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="e39e6-153">Get-AzureIPForwarding</span></span>](./Get-AzureIPForwarding.md)
