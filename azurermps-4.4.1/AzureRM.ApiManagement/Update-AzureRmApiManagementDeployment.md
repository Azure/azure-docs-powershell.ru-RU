---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: e4170dbe2a1ac4ed8ad39bdb7a5db6d7174555e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557972"
---
# <span data-ttu-id="00085-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="00085-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="00085-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00085-102">SYNOPSIS</span></span>
<span data-ttu-id="00085-103">Обновляет развертывание службы управления API.</span><span class="sxs-lookup"><span data-stu-id="00085-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00085-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00085-104">SYNTAX</span></span>

### <span data-ttu-id="00085-105">Определенная служба управления API (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="00085-105">Specific API Management service (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00085-106">Обновление из экземпляра PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="00085-106">Update from PsApiManagement instance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00085-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00085-107">DESCRIPTION</span></span>
<span data-ttu-id="00085-108">Командлет **Update-AzureRmApiManagementDeployment** обновляет текущие развертывания службы управления API.</span><span class="sxs-lookup"><span data-stu-id="00085-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="00085-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00085-109">EXAMPLES</span></span>

### <span data-ttu-id="00085-110">Пример 1: Обновление развертывания экземпляра ApiManagement</span><span class="sxs-lookup"><span data-stu-id="00085-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="00085-111">Эта команда обновляет развертывание экземпляра управления API до трех стандартных мощностей устройства.</span><span class="sxs-lookup"><span data-stu-id="00085-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="00085-112">Пример 2: получение экземпляра ApiManagement и его изменение масштаба</span><span class="sxs-lookup"><span data-stu-id="00085-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="00085-113">В этом примере выполняется получение экземпляра управления API, масштабируется до пяти единиц измерения Premium, а затем в привилегированную область добавляются дополнительные три устройства.</span><span class="sxs-lookup"><span data-stu-id="00085-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="00085-114">Пример 3: развертывание обновления (внешняя виртуальная сеть)</span><span class="sxs-lookup"><span data-stu-id="00085-114">Example 3: Update deployment (external VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="00085-115">Эта команда обновляет существующее развертывание управления API и присоединяется к внешнему *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="00085-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="00085-116">Пример 4: развертывание обновления (Внутренняя виртуальная сеть)</span><span class="sxs-lookup"><span data-stu-id="00085-116">Example 4: Update deployment (internal VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="00085-117">Эта команда обновляет существующее развертывание управления API и присоединяется к внутренней *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="00085-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="00085-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00085-118">PARAMETERS</span></span>

### <span data-ttu-id="00085-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="00085-119">-AdditionalRegions</span></span>
<span data-ttu-id="00085-120">Задает дополнительные области развертывания для управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="00085-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00085-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="00085-121">-ApiManagement</span></span>
<span data-ttu-id="00085-122">Указывает экземпляр **PsApiManagement** , для которого требуется получить конфигурацию развертывания.</span><span class="sxs-lookup"><span data-stu-id="00085-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="00085-123">Используйте этот параметр, если в экземпляре уже есть все необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="00085-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: Update from PsApiManagement instance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00085-124">-Capacity</span><span class="sxs-lookup"><span data-stu-id="00085-124">-Capacity</span></span>
<span data-ttu-id="00085-125">Указывает емкость SKU основного региона развертывания управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="00085-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00085-126">-Location</span><span class="sxs-lookup"><span data-stu-id="00085-126">-Location</span></span>
<span data-ttu-id="00085-127">Указывает расположение области развертывания для основного API-управления.</span><span class="sxs-lookup"><span data-stu-id="00085-127">Specifies the location of the master API Management deployment region.</span></span>

<span data-ttu-id="00085-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="00085-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="00085-129">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="00085-129">North Central US</span></span>
- <span data-ttu-id="00085-130">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="00085-130">South Central US</span></span>
- <span data-ttu-id="00085-131">Центральная американская</span><span class="sxs-lookup"><span data-stu-id="00085-131">Central US</span></span>
- <span data-ttu-id="00085-132">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="00085-132">West Europe</span></span>
- <span data-ttu-id="00085-133">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="00085-133">North Europe</span></span>
- <span data-ttu-id="00085-134">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="00085-134">West US</span></span>
- <span data-ttu-id="00085-135">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="00085-135">East US</span></span>
- <span data-ttu-id="00085-136">Восточная часть 2</span><span class="sxs-lookup"><span data-stu-id="00085-136">East US 2</span></span>
- <span data-ttu-id="00085-137">Восточная Япония</span><span class="sxs-lookup"><span data-stu-id="00085-137">Japan East</span></span>
- <span data-ttu-id="00085-138">Западная часть Японии</span><span class="sxs-lookup"><span data-stu-id="00085-138">Japan West</span></span>
- <span data-ttu-id="00085-139">Южная Бразилия</span><span class="sxs-lookup"><span data-stu-id="00085-139">Brazil South</span></span>
- <span data-ttu-id="00085-140">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="00085-140">Southeast Asia</span></span>
- <span data-ttu-id="00085-141">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="00085-141">East Asia</span></span>
- <span data-ttu-id="00085-142">Восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="00085-142">Australia East</span></span>
- <span data-ttu-id="00085-143">Юго-восток Австралии</span><span class="sxs-lookup"><span data-stu-id="00085-143">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00085-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="00085-144">-Name</span></span>
<span data-ttu-id="00085-145">Указывает имя управления API, которое обновляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="00085-145">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00085-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00085-146">-PassThru</span></span>
<span data-ttu-id="00085-147">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="00085-147">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="00085-148">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="00085-148">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00085-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00085-149">-ResourceGroupName</span></span>
<span data-ttu-id="00085-150">Указывает имя группы ресурсов, для которой существует управление API.</span><span class="sxs-lookup"><span data-stu-id="00085-150">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00085-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="00085-151">-Sku</span></span>
<span data-ttu-id="00085-152">Указывает уровень области развертывания главного Azure Management API.</span><span class="sxs-lookup"><span data-stu-id="00085-152">Specifies the tier of the master Azure API Management deployment region.</span></span>

<span data-ttu-id="00085-153">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="00085-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="00085-154">Программист</span><span class="sxs-lookup"><span data-stu-id="00085-154">Developer</span></span>
- <span data-ttu-id="00085-155">Стандартная</span><span class="sxs-lookup"><span data-stu-id="00085-155">Standard</span></span>
- <span data-ttu-id="00085-156">Версию</span><span class="sxs-lookup"><span data-stu-id="00085-156">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00085-157">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="00085-157">-VirtualNetwork</span></span>
<span data-ttu-id="00085-158">Указывает конфигурацию виртуальной сети для главного региона развертывания управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="00085-158">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00085-159">-VpnType</span><span class="sxs-lookup"><span data-stu-id="00085-159">-VpnType</span></span>
<span data-ttu-id="00085-160">Указывает тип виртуальной сети для развертывания управления API.</span><span class="sxs-lookup"><span data-stu-id="00085-160">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="00085-161">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="00085-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="00085-162">Ничего.</span><span class="sxs-lookup"><span data-stu-id="00085-162">None.</span></span>
<span data-ttu-id="00085-163">Развертывание управления API не является частью какой-либо виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="00085-163">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="00085-164">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="00085-164">This is the default value.</span></span> 
- <span data-ttu-id="00085-165">Внешние.</span><span class="sxs-lookup"><span data-stu-id="00085-165">External.</span></span>
<span data-ttu-id="00085-166">Развертывание управления API имеет внешний виртуальный адрес, который находится в сети.</span><span class="sxs-lookup"><span data-stu-id="00085-166">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="00085-167">Программой.</span><span class="sxs-lookup"><span data-stu-id="00085-167">Internal.</span></span>
<span data-ttu-id="00085-168">В развертывании управления API есть виртуальный адрес, подключенный к интрасети.</span><span class="sxs-lookup"><span data-stu-id="00085-168">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00085-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00085-169">-DefaultProfile</span></span>
<span data-ttu-id="00085-170">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00085-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00085-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00085-171">CommonParameters</span></span>
<span data-ttu-id="00085-172">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00085-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00085-173">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00085-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00085-174">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00085-174">INPUTS</span></span>

### <span data-ttu-id="00085-175">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="00085-175">PsApiManagement</span></span>
<span data-ttu-id="00085-176">Параметр "ApiManagement" принимает значение типа "PsApiManagement" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="00085-176">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="00085-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00085-177">OUTPUTS</span></span>

### <span data-ttu-id="00085-178">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="00085-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="00085-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="00085-179">NOTES</span></span>

## <span data-ttu-id="00085-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00085-180">RELATED LINKS</span></span>

[<span data-ttu-id="00085-181">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="00085-181">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


