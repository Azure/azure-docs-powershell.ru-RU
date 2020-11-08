---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8418A93-8E6B-4A1C-B319-7CACE95AB600
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1daf0cb8881beeb71f0b3fe68732d596c56ce12
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076240"
---
# <span data-ttu-id="5e526-101">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="5e526-101">Move-AzureService</span></span>

## <span data-ttu-id="5e526-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e526-102">SYNOPSIS</span></span>
<span data-ttu-id="5e526-103">Переносит облачную службу в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5e526-103">Migrates a cloud service to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="5e526-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e526-104">SYNTAX</span></span>

### <span data-ttu-id="5e526-105">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e526-105">AbortMigrationParameterSet</span></span>
```
Move-AzureService [-Abort] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5e526-106">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e526-106">CommitMigrationParameterSet</span></span>
```
Move-AzureService [-Commit] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5e526-107">PrepareNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e526-107">PrepareNewMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e526-108">PrepareExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e526-108">PrepareExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e526-109">ValidateNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e526-109">ValidateNewMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e526-110">ValidateExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e526-110">ValidateExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e526-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e526-111">DESCRIPTION</span></span>
<span data-ttu-id="5e526-112">Командлет **Move-AzureService** переносит облачную службу и развертывание внутри этой службы в группу ресурсов в стеке диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5e526-112">The **Move-AzureService** cmdlet migrates a cloud service and a deployment inside that service to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="5e526-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e526-113">EXAMPLES</span></span>

### <span data-ttu-id="5e526-114">Пример 1: подготовка миграции служб</span><span class="sxs-lookup"><span data-stu-id="5e526-114">Example 1: Prepare service migration</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="5e526-115">Эта команда подготавливает службу с именем ContosoService для миграции в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5e526-115">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="5e526-116">Миграция включает развертывание с именем ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="5e526-116">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="5e526-117">Пример 2: Запуск миграции служб</span><span class="sxs-lookup"><span data-stu-id="5e526-117">Example 2: Start service migration</span></span>
```
PS C:\> Move-AzureService -Commit -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="5e526-118">Эта команда запускает миграцию службы с именем ContosoService в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5e526-118">This command starts migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="5e526-119">Миграция включает развертывание с именем ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="5e526-119">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="5e526-120">Пример 3: Отмена миграции служб</span><span class="sxs-lookup"><span data-stu-id="5e526-120">Example 3: Cancel service migration</span></span>
```
PS C:\> Move-AzureService -Abort -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="5e526-121">Эта команда отменяет миграцию службы с именем ContosoService в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5e526-121">This command cancels migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="5e526-122">Пример 4: подготовка миграции служб к существующей виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="5e526-122">Example 4: Prepare service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "VnetRG" -VirtualNetworkName "ContosoVNET" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="5e526-123">Эта команда подготавливает службу с именем ContosoService для миграции в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5e526-123">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="5e526-124">Миграция включает развертывание с именем ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="5e526-124">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="5e526-125">Миграция использует виртуальную сеть, созданную ранее.</span><span class="sxs-lookup"><span data-stu-id="5e526-125">The migration uses a virtual network that was previously created.</span></span>

### <span data-ttu-id="5e526-126">Пример 5: Проверка миграции служб</span><span class="sxs-lookup"><span data-stu-id="5e526-126">Example 5: Validate service migration</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="5e526-127">Эта команда проверяет миграцию для службы с именем ContosoService в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5e526-127">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="5e526-128">Миграция включает развертывание с именем ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="5e526-128">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="5e526-129">Пример 6: Проверка миграции служб на существующую виртуальную сеть</span><span class="sxs-lookup"><span data-stu-id="5e526-129">Example 6: Validate service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "contosoService" -DeploymentName "contosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "vnetRG" -VirtualNetworkName "contosoVNET" -SubnetName "contosoSubnet"
```

<span data-ttu-id="5e526-130">Эта команда проверяет миграцию для службы с именем ContosoService в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5e526-130">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="5e526-131">Миграция включает развертывание с именем ContosoVM.</span><span class="sxs-lookup"><span data-stu-id="5e526-131">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="5e526-132">Миграция использует виртуальную сеть, созданную ранее.</span><span class="sxs-lookup"><span data-stu-id="5e526-132">The migration uses a virtual network that was previously created.</span></span>

## <span data-ttu-id="5e526-133">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e526-133">PARAMETERS</span></span>

### <span data-ttu-id="5e526-134">-Abort</span><span class="sxs-lookup"><span data-stu-id="5e526-134">-Abort</span></span>
<span data-ttu-id="5e526-135">Указывает, что этот командлет отменяет миграцию служб.</span><span class="sxs-lookup"><span data-stu-id="5e526-135">Indicates that this cmdlet cancels the service migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e526-136">-Commit</span><span class="sxs-lookup"><span data-stu-id="5e526-136">-Commit</span></span>
<span data-ttu-id="5e526-137">Указывает на то, что этот командлет запускает миграцию служб.</span><span class="sxs-lookup"><span data-stu-id="5e526-137">Indicates that this cmdlet starts the service migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e526-138">-CreateNewVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5e526-138">-CreateNewVirtualNetwork</span></span>
<span data-ttu-id="5e526-139">Указывает на то, что этот командлет создает виртуальную сеть в стеке диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5e526-139">Indicates that this cmdlet creates a virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, ValidateNewMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e526-140">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="5e526-140">-DeploymentName</span></span>
<span data-ttu-id="5e526-141">Указывает имя развертывания облачной службы, которое переносит этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5e526-141">Specifies the name of the cloud service deployment that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e526-142">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5e526-142">-InformationAction</span></span>
<span data-ttu-id="5e526-143">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="5e526-143">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5e526-144">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5e526-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5e526-145">Продолжал</span><span class="sxs-lookup"><span data-stu-id="5e526-145">Continue</span></span>
- <span data-ttu-id="5e526-146">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="5e526-146">Ignore</span></span>
- <span data-ttu-id="5e526-147">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="5e526-147">Inquire</span></span>
- <span data-ttu-id="5e526-148">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5e526-148">SilentlyContinue</span></span>
- <span data-ttu-id="5e526-149">Остановить</span><span class="sxs-lookup"><span data-stu-id="5e526-149">Stop</span></span>
- <span data-ttu-id="5e526-150">Рвать</span><span class="sxs-lookup"><span data-stu-id="5e526-150">Suspend</span></span>

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

### <span data-ttu-id="5e526-151">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5e526-151">-InformationVariable</span></span>
<span data-ttu-id="5e526-152">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="5e526-152">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5e526-153">-Подготовка</span><span class="sxs-lookup"><span data-stu-id="5e526-153">-Prepare</span></span>
<span data-ttu-id="5e526-154">Указывает на то, что этот командлет подготавливает облачную службу для миграции.</span><span class="sxs-lookup"><span data-stu-id="5e526-154">Indicates that this cmdlet prepares the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, PrepareExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e526-155">-Profile</span><span class="sxs-lookup"><span data-stu-id="5e526-155">-Profile</span></span>
<span data-ttu-id="5e526-156">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5e526-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5e526-157">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5e526-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5e526-158">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5e526-158">-ServiceName</span></span>
<span data-ttu-id="5e526-159">Указывает имя облачной службы, которая переносится этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5e526-159">Specifies the name  of the cloud service that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e526-160">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="5e526-160">-SubnetName</span></span>
<span data-ttu-id="5e526-161">Указывает имя подсети внутри виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5e526-161">Specifies the name of the Subnet inside the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e526-162">-UseExistingVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5e526-162">-UseExistingVirtualNetwork</span></span>
<span data-ttu-id="5e526-163">Указывает на то, что этот командлет переносит облачную службу в существующую виртуальную сеть в стеке диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5e526-163">Indicates that this cmdlet migrates the cloud service to an existing virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e526-164">-Проверка</span><span class="sxs-lookup"><span data-stu-id="5e526-164">-Validate</span></span>
<span data-ttu-id="5e526-165">Указывает, что этот командлет проверяет облачную службу для миграции.</span><span class="sxs-lookup"><span data-stu-id="5e526-165">Specifies that this cmdlet validates the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateNewMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e526-166">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5e526-166">-VirtualNetworkName</span></span>
<span data-ttu-id="5e526-167">Указывает имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5e526-167">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e526-168">-VirtualNetworkResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e526-168">-VirtualNetworkResourceGroupName</span></span>
<span data-ttu-id="5e526-169">Указывает имя группы ресурсов для существующей виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5e526-169">Specifies the name of the resource group of an existing virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e526-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e526-170">CommonParameters</span></span>
<span data-ttu-id="5e526-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e526-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e526-172">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e526-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e526-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e526-173">INPUTS</span></span>

## <span data-ttu-id="5e526-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e526-174">OUTPUTS</span></span>

## <span data-ttu-id="5e526-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e526-175">NOTES</span></span>

## <span data-ttu-id="5e526-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e526-176">RELATED LINKS</span></span>

[<span data-ttu-id="5e526-177">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5e526-177">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="5e526-178">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="5e526-178">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="5e526-179">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="5e526-179">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="5e526-180">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5e526-180">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="5e526-181">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5e526-181">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


