---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: 2d79857df255bb960c51b87c536013921f3b1c00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997993"
---
# <span data-ttu-id="0f64c-101">Get-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="0f64c-101">Get-AzIotCentralApp</span></span>

## <span data-ttu-id="0f64c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f64c-102">SYNOPSIS</span></span>
<span data-ttu-id="0f64c-103">Свойства одного или нескольких центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="0f64c-103">Gets properties for either one or several IoT Central Applications.</span></span>

## <span data-ttu-id="0f64c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0f64c-104">SYNTAX</span></span>

### <span data-ttu-id="0f64c-105">ListIotCentralAppsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f64c-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f64c-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f64c-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f64c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f64c-107">ResourceIdParameterSet</span></span>
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f64c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f64c-108">DESCRIPTION</span></span>
<span data-ttu-id="0f64c-109">Возвращает метаданные для определенного центрального приложения IoT или всех приложений в группе ресурсов или подписке в зависимости от набора параметров.</span><span class="sxs-lookup"><span data-stu-id="0f64c-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="0f64c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0f64c-110">EXAMPLES</span></span>

### <span data-ttu-id="0f64c-111">Пример 1. Получение определенного центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="0f64c-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="0f64c-112">Возвращает метаданные для указанного центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="0f64c-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="0f64c-113">Пример выходных данных:</span><span class="sxs-lookup"><span data-stu-id="0f64c-113">Example Output:</span></span>

<span data-ttu-id="0f64c-114">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f64c-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="0f64c-115">Пример 2. Получение центрального приложения IoT в подписке.</span><span class="sxs-lookup"><span data-stu-id="0f64c-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp
```

<span data-ttu-id="0f64c-116">Возвращает метаданные для всех центрального приложений IoT в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="0f64c-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="0f64c-117">Пример выходных данных:</span><span class="sxs-lookup"><span data-stu-id="0f64c-117">Example Output:</span></span>

<span data-ttu-id="0f64c-118">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f64c-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="0f64c-119">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName2 Name : MyAppResourceName2 Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXX DisplayName: My Custom Display Name 2 Subdomain : MyAppSubdomain2 Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span><span class="sxs-lookup"><span data-stu-id="0f64c-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="0f64c-120">Пример 3. Получение центрального приложения IoT в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f64c-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="0f64c-121">Возвращает метаданные для всех центрального приложений IoT в предоставленной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f64c-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="0f64c-122">Пример выходных данных:</span><span class="sxs-lookup"><span data-stu-id="0f64c-122">Example Output:</span></span>

<span data-ttu-id="0f64c-123">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName Name : MyAppResourceName Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXXXXXXX DisplayName : My Custom Display Name Subdomain : MyAppSubdomain Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f64c-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="0f64c-124">ResourceId : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft . IoTCentral/IoTApps/MyAppResourceName2 Name : MyAppResourceName2 Type : Microsoft.IoTCentral/IoTApps Location : westus Tag : {[key, val]} SKU : Microsoft.Azure.Commands.iotCentral.Models.PSIotCentralAppSkuInfo ApplicationId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXX DisplayName : My Custom Display Name 2 Subdomain : MyAppSubdomain2 Template : iotc-default@1.0.0 SubscriptionId : XXXXXXXX-XXXX-XXXX-XXXXXXXXXX ResourceGroupName : MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f64c-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="0f64c-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f64c-125">PARAMETERS</span></span>

### <span data-ttu-id="0f64c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f64c-126">-DefaultProfile</span></span>
<span data-ttu-id="0f64c-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f64c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f64c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="0f64c-128">-Name</span></span>
<span data-ttu-id="0f64c-129">Имя центрального ресурса приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="0f64c-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f64c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f64c-130">-ResourceGroupName</span></span>
<span data-ttu-id="0f64c-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f64c-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f64c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f64c-132">-ResourceId</span></span>
<span data-ttu-id="0f64c-133">Iot Central Application Resource Id.</span><span class="sxs-lookup"><span data-stu-id="0f64c-133">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f64c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f64c-134">CommonParameters</span></span>
<span data-ttu-id="0f64c-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f64c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f64c-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f64c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f64c-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f64c-137">INPUTS</span></span>

### <span data-ttu-id="0f64c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0f64c-138">System.String</span></span>

## <span data-ttu-id="0f64c-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0f64c-139">OUTPUTS</span></span>

### <span data-ttu-id="0f64c-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="0f64c-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="0f64c-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0f64c-141">NOTES</span></span>

## <span data-ttu-id="0f64c-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f64c-142">RELATED LINKS</span></span>
