---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: f8f0273ab624cd81488734f9b84debc045f6fed2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558592"
---
# <span data-ttu-id="c11ad-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="c11ad-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="c11ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c11ad-102">SYNOPSIS</span></span>
<span data-ttu-id="c11ad-103">Обновляет развертывание службы управления API.</span><span class="sxs-lookup"><span data-stu-id="c11ad-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c11ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c11ad-104">SYNTAX</span></span>

### <span data-ttu-id="c11ad-105">UpdateSpecificService (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c11ad-105">UpdateSpecificService (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c11ad-106">UpdateFromPsApiManagementInstance</span><span class="sxs-lookup"><span data-stu-id="c11ad-106">UpdateFromPsApiManagementInstance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c11ad-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c11ad-107">DESCRIPTION</span></span>
<span data-ttu-id="c11ad-108">Командлет **Update-AzureRmApiManagementDeployment** обновляет текущие развертывания службы управления API.</span><span class="sxs-lookup"><span data-stu-id="c11ad-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="c11ad-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c11ad-109">EXAMPLES</span></span>

### <span data-ttu-id="c11ad-110">Пример 1: Обновление развертывания экземпляра ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c11ad-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```powershell
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="c11ad-111">Эта команда обновляет развертывание экземпляра управления API до трех стандартных мощностей устройства.</span><span class="sxs-lookup"><span data-stu-id="c11ad-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="c11ad-112">Пример 2: получение экземпляра ApiManagement и его изменение масштаба</span><span class="sxs-lookup"><span data-stu-id="c11ad-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```powershell
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="c11ad-113">В этом примере выполняется получение экземпляра управления API, масштабируется до пяти единиц измерения Premium, а затем в привилегированную область добавляются дополнительные три устройства.</span><span class="sxs-lookup"><span data-stu-id="c11ad-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="c11ad-114">Пример 3: развертывание обновления (внешняя виртуальная сеть)</span><span class="sxs-lookup"><span data-stu-id="c11ad-114">Example 3: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="c11ad-115">Эта команда обновляет существующее развертывание управления API и присоединяется к внешнему *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="c11ad-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="c11ad-116">Пример 4: развертывание обновления (Внутренняя виртуальная сеть)</span><span class="sxs-lookup"><span data-stu-id="c11ad-116">Example 4: Update deployment (internal VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="c11ad-117">Эта команда обновляет существующее развертывание управления API и присоединяется к внутренней *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="c11ad-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="c11ad-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c11ad-118">PARAMETERS</span></span>

### <span data-ttu-id="c11ad-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="c11ad-119">-AdditionalRegions</span></span>
<span data-ttu-id="c11ad-120">Задает дополнительные области развертывания для управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="c11ad-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11ad-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c11ad-121">-ApiManagement</span></span>
<span data-ttu-id="c11ad-122">Указывает экземпляр **PsApiManagement** , для которого требуется получить конфигурацию развертывания.</span><span class="sxs-lookup"><span data-stu-id="c11ad-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="c11ad-123">Используйте этот параметр, если в экземпляре уже есть все необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="c11ad-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: UpdateFromPsApiManagementInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c11ad-124">-Capacity</span><span class="sxs-lookup"><span data-stu-id="c11ad-124">-Capacity</span></span>
<span data-ttu-id="c11ad-125">Указывает емкость SKU основного региона развертывания управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="c11ad-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11ad-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c11ad-126">-DefaultProfile</span></span>
<span data-ttu-id="c11ad-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c11ad-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c11ad-128">-Location</span><span class="sxs-lookup"><span data-stu-id="c11ad-128">-Location</span></span>
<span data-ttu-id="c11ad-129">Указывает расположение области развертывания для основного API-управления.</span><span class="sxs-lookup"><span data-stu-id="c11ad-129">Specifies the location of the master API Management deployment region.</span></span>
<span data-ttu-id="c11ad-130">Для получения допустимых местоположений используйте командлет Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "Service"} | Расположение Select-Object</span><span class="sxs-lookup"><span data-stu-id="c11ad-130">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11ad-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c11ad-131">-Name</span></span>
<span data-ttu-id="c11ad-132">Указывает имя управления API, которое обновляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c11ad-132">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11ad-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c11ad-133">-PassThru</span></span>
<span data-ttu-id="c11ad-134">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="c11ad-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c11ad-135">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c11ad-135">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c11ad-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c11ad-136">-ResourceGroupName</span></span>
<span data-ttu-id="c11ad-137">Указывает имя группы ресурсов, для которой существует управление API.</span><span class="sxs-lookup"><span data-stu-id="c11ad-137">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11ad-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="c11ad-138">-Sku</span></span>
<span data-ttu-id="c11ad-139">Указывает уровень области развертывания главного Azure Management API.</span><span class="sxs-lookup"><span data-stu-id="c11ad-139">Specifies the tier of the master Azure API Management deployment region.</span></span>
<span data-ttu-id="c11ad-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c11ad-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c11ad-141">Программист</span><span class="sxs-lookup"><span data-stu-id="c11ad-141">Developer</span></span>
- <span data-ttu-id="c11ad-142">Стандартная</span><span class="sxs-lookup"><span data-stu-id="c11ad-142">Standard</span></span>
- <span data-ttu-id="c11ad-143">Версию</span><span class="sxs-lookup"><span data-stu-id="c11ad-143">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11ad-144">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c11ad-144">-VirtualNetwork</span></span>
<span data-ttu-id="c11ad-145">Указывает конфигурацию виртуальной сети для главного региона развертывания управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="c11ad-145">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11ad-146">-VpnType</span><span class="sxs-lookup"><span data-stu-id="c11ad-146">-VpnType</span></span>
<span data-ttu-id="c11ad-147">Указывает тип виртуальной сети для развертывания управления API.</span><span class="sxs-lookup"><span data-stu-id="c11ad-147">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="c11ad-148">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c11ad-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c11ad-149">Ничего.</span><span class="sxs-lookup"><span data-stu-id="c11ad-149">None.</span></span>
<span data-ttu-id="c11ad-150">Развертывание управления API не является частью какой-либо виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c11ad-150">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="c11ad-151">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c11ad-151">This is the default value.</span></span> 
- <span data-ttu-id="c11ad-152">Внешние.</span><span class="sxs-lookup"><span data-stu-id="c11ad-152">External.</span></span>
<span data-ttu-id="c11ad-153">Развертывание управления API имеет внешний виртуальный адрес, который находится в сети.</span><span class="sxs-lookup"><span data-stu-id="c11ad-153">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="c11ad-154">Программой.</span><span class="sxs-lookup"><span data-stu-id="c11ad-154">Internal.</span></span>
<span data-ttu-id="c11ad-155">В развертывании управления API есть виртуальный адрес, подключенный к интрасети.</span><span class="sxs-lookup"><span data-stu-id="c11ad-155">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11ad-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c11ad-156">CommonParameters</span></span>
<span data-ttu-id="c11ad-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c11ad-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c11ad-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c11ad-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c11ad-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c11ad-159">INPUTS</span></span>

### <span data-ttu-id="c11ad-160">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c11ad-160">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="c11ad-161">Параметры: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c11ad-161">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="c11ad-162">System. String</span><span class="sxs-lookup"><span data-stu-id="c11ad-162">System.String</span></span>

### <span data-ttu-id="c11ad-163">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="c11ad-163">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="c11ad-164">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c11ad-164">System.Int32</span></span>

### <span data-ttu-id="c11ad-165">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c11ad-165">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="c11ad-166">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVpnType</span><span class="sxs-lookup"><span data-stu-id="c11ad-166">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType</span></span>

### <span data-ttu-id="c11ad-167">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion, Microsoft. Azure. Commands. ApiManagement, Version = 6.1.2.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="c11ad-167">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion, Microsoft.Azure.Commands.ApiManagement, Version=6.1.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c11ad-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c11ad-168">OUTPUTS</span></span>

### <span data-ttu-id="c11ad-169">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c11ad-169">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c11ad-170">Пуск</span><span class="sxs-lookup"><span data-stu-id="c11ad-170">NOTES</span></span>

## <span data-ttu-id="c11ad-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c11ad-171">RELATED LINKS</span></span>

[<span data-ttu-id="c11ad-172">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c11ad-172">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


