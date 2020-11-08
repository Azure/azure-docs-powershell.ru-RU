---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 64639A35-0573-48C8-AB21-19FEB09537BA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b1b251a5fef3ad91f830e18714796421d2abca7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075758"
---
# <span data-ttu-id="aae38-101">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="aae38-101">Set-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="aae38-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aae38-102">SYNOPSIS</span></span>
<span data-ttu-id="aae38-103">Применяет сетевую группу безопасности к виртуальной машине, роли PaaS или сетевому адаптеру.</span><span class="sxs-lookup"><span data-stu-id="aae38-103">Associates a network security group to a virtual machine, PaaS role, or network adapter.</span></span>

## <span data-ttu-id="aae38-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aae38-104">SYNTAX</span></span>

### <span data-ttu-id="aae38-105">AddNetworkSecurityGroupAssociationToSubnet</span><span class="sxs-lookup"><span data-stu-id="aae38-105">AddNetworkSecurityGroupAssociationToSubnet</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VirtualNetworkName <String>
 -SubnetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="aae38-106">AddNetworkSecurityGroupAssociationToIaaSRole</span><span class="sxs-lookup"><span data-stu-id="aae38-106">AddNetworkSecurityGroupAssociationToIaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VM <PersistentVMRoleContext>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="aae38-107">AddNetworkSecurityGroupAssociationToPaaSRole</span><span class="sxs-lookup"><span data-stu-id="aae38-107">AddNetworkSecurityGroupAssociationToPaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] [-Slot <String>]
 -RoleName <String> -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="aae38-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aae38-108">DESCRIPTION</span></span>
<span data-ttu-id="aae38-109">Командлет **Set-AzureNetworkSecurityGroupAssociation** связывает группу безопасности сети с виртуальной машиной, платформой как ролью службы (PaaS) или сетевым адаптером.</span><span class="sxs-lookup"><span data-stu-id="aae38-109">The **Set-AzureNetworkSecurityGroupAssociation** cmdlet associates a network security group to a virtual machine, platform as a service (PaaS) role, or network adapter.</span></span>

## <span data-ttu-id="aae38-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aae38-110">EXAMPLES</span></span>

### <span data-ttu-id="aae38-111">Пример 1: назначение виртуальной машины сетевой группе безопасности</span><span class="sxs-lookup"><span data-stu-id="aae38-111">Example 1: Assign a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="aae38-112">Эта команда получает виртуальную машину с именем ContosoVM06 для службы с именем ContosoService и передает этот объект виртуальной машины в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="aae38-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="aae38-113">Текущий командлет назначает сетевую группу безопасности с именем ContosoNetworkSecurityGroup на эту виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="aae38-113">The current cmdlet assigns the network security group named ContosoNetworkSecurityGroup to that virtual machine.</span></span>

## <span data-ttu-id="aae38-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aae38-114">PARAMETERS</span></span>

### <span data-ttu-id="aae38-115">-Force</span><span class="sxs-lookup"><span data-stu-id="aae38-115">-Force</span></span>
<span data-ttu-id="aae38-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="aae38-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aae38-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aae38-117">-Name</span></span>
<span data-ttu-id="aae38-118">Указывает имя сетевой группы безопасности, которую задает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="aae38-118">Specifies the name of the network security group that this cmdlet sets.</span></span>

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

### <span data-ttu-id="aae38-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="aae38-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="aae38-120">Указывает имя сетевого адаптера, к которому этот командлет применяет сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="aae38-120">Specifies the name of the network adapter to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae38-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aae38-121">-PassThru</span></span>
<span data-ttu-id="aae38-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="aae38-122">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="aae38-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="aae38-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aae38-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="aae38-124">-Profile</span></span>
<span data-ttu-id="aae38-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="aae38-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="aae38-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aae38-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aae38-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="aae38-127">-RoleName</span></span>
<span data-ttu-id="aae38-128">Указывает имя роли PaaS, к которой этот командлет применяет сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="aae38-128">Specifies the name of a PaaS role to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae38-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="aae38-129">-ServiceName</span></span>
<span data-ttu-id="aae38-130">Указывает имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="aae38-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="aae38-131">Роль PaaS принадлежит службе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="aae38-131">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae38-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="aae38-132">-Slot</span></span>
<span data-ttu-id="aae38-133">Указывает гнездо PaaS.</span><span class="sxs-lookup"><span data-stu-id="aae38-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="aae38-134">Роль PaaS, для которой этот командлет задает сетевую группу безопасности, имеет область, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="aae38-134">The PaaS role for which this cmdlet sets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="aae38-135">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="aae38-135">Valid values are:</span></span> 

- <span data-ttu-id="aae38-136">Спецификации</span><span class="sxs-lookup"><span data-stu-id="aae38-136">Production</span></span>
- <span data-ttu-id="aae38-137">Промежуточного хранения</span><span class="sxs-lookup"><span data-stu-id="aae38-137">Staging</span></span> 

<span data-ttu-id="aae38-138">Значением по умолчанию является "производство".</span><span class="sxs-lookup"><span data-stu-id="aae38-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae38-139">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="aae38-139">-SubnetName</span></span>
<span data-ttu-id="aae38-140">Указывает имя подсети, в которую этот командлет связывает сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="aae38-140">Specifies the name of a subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae38-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="aae38-141">-VirtualNetworkName</span></span>
<span data-ttu-id="aae38-142">Указывает имя виртуальной сети, содержащей подсеть, в которую этот командлет связывается с группой безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="aae38-142">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae38-143">-VM</span><span class="sxs-lookup"><span data-stu-id="aae38-143">-VM</span></span>
<span data-ttu-id="aae38-144">Указывает виртуальную машину, к которой этот командлет применяет сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="aae38-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aae38-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae38-145">CommonParameters</span></span>
<span data-ttu-id="aae38-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aae38-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae38-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aae38-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae38-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aae38-148">INPUTS</span></span>

## <span data-ttu-id="aae38-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aae38-149">OUTPUTS</span></span>

### <span data-ttu-id="aae38-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aae38-150">System.Boolean</span></span>

## <span data-ttu-id="aae38-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="aae38-151">NOTES</span></span>

## <span data-ttu-id="aae38-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aae38-152">RELATED LINKS</span></span>

[<span data-ttu-id="aae38-153">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="aae38-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="aae38-154">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="aae38-154">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)


