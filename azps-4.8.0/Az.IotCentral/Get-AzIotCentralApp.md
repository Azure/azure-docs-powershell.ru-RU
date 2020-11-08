---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: cbc7e255f74943ea2aff3518d278035f72394235
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236677"
---
# <span data-ttu-id="47106-101">Get-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="47106-101">Get-AzIotCentralApp</span></span>

## <span data-ttu-id="47106-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47106-102">SYNOPSIS</span></span>
<span data-ttu-id="47106-103">Возвращает свойства для одного или нескольких приложений Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="47106-103">Gets properties for either one or several IoT Central Applications.</span></span>

## <span data-ttu-id="47106-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47106-104">SYNTAX</span></span>

### <span data-ttu-id="47106-105">ListIotCentralAppsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="47106-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47106-106">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="47106-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47106-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47106-107">ResourceIdParameterSet</span></span>
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47106-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47106-108">DESCRIPTION</span></span>
<span data-ttu-id="47106-109">Получение метаданных для определенного центра администрирования Интернет вещей или всех приложений в группе ресурсов или подписке в зависимости от множества параметров.</span><span class="sxs-lookup"><span data-stu-id="47106-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="47106-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47106-110">EXAMPLES</span></span>

### <span data-ttu-id="47106-111">Пример 1. Загрузите конкретное центральное приложение IoT.</span><span class="sxs-lookup"><span data-stu-id="47106-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="47106-112">Получает метаданные для указанного приложения центра администрирования Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="47106-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="47106-113">Пример вывода:</span><span class="sxs-lookup"><span data-stu-id="47106-113">Example Output:</span></span>

<span data-ttu-id="47106-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName имя: MyAppResourceName тип: Microsoft. IoTCentral/IoTApps расположение: westus тег: {[key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My My имя домена: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX: ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47106-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="47106-115">Пример 2. получение центральных приложений IoT в подписке.</span><span class="sxs-lookup"><span data-stu-id="47106-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp
```

<span data-ttu-id="47106-116">Получает метаданные для всех центральных приложений IoT в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="47106-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="47106-117">Пример вывода:</span><span class="sxs-lookup"><span data-stu-id="47106-117">Example Output:</span></span>

<span data-ttu-id="47106-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName имя: MyAppResourceName тип: Microsoft. IoTCentral/IoTApps расположение: westus тег: {[key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My My имя домена: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX: ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47106-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="47106-119">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 имя: MyAppResourceName2 тип: Microsoft. IoTCentral/IoTApps расположение: westus тег: {[key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My личное отображаемое имя 2 поддомен: MyAppSubdomain2 Template: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX.</span><span class="sxs-lookup"><span data-stu-id="47106-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="47106-120">Пример 3 получение центральных приложений IoT в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47106-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="47106-121">Получает метаданные для всех центральных приложений IoT в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47106-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="47106-122">Пример вывода:</span><span class="sxs-lookup"><span data-stu-id="47106-122">Example Output:</span></span>

<span data-ttu-id="47106-123">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName имя: MyAppResourceName тип: Microsoft. IoTCentral/IoTApps расположение: westus тег: {[key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My My имя домена: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX: ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47106-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="47106-124">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName2 имя: MyAppResourceName2 тип: Microsoft. IoTCentral/IoTApps расположение: westus тег: {[key, Val]} SKU: Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My личное отображаемое имя 2 поддомен: MyAppSubdomain2 Template: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX.</span><span class="sxs-lookup"><span data-stu-id="47106-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="47106-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47106-125">PARAMETERS</span></span>

### <span data-ttu-id="47106-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47106-126">-DefaultProfile</span></span>
<span data-ttu-id="47106-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47106-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47106-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="47106-128">-Name</span></span>
<span data-ttu-id="47106-129">Имя ресурса центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="47106-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="47106-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47106-130">-ResourceGroupName</span></span>
<span data-ttu-id="47106-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47106-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="47106-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47106-132">-ResourceId</span></span>
<span data-ttu-id="47106-133">Идентификатор ресурса приложения центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="47106-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="47106-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47106-134">CommonParameters</span></span>
<span data-ttu-id="47106-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47106-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47106-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47106-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47106-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47106-137">INPUTS</span></span>

### <span data-ttu-id="47106-138">System. String</span><span class="sxs-lookup"><span data-stu-id="47106-138">System.String</span></span>

## <span data-ttu-id="47106-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47106-139">OUTPUTS</span></span>

### <span data-ttu-id="47106-140">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="47106-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="47106-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="47106-141">NOTES</span></span>

## <span data-ttu-id="47106-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47106-142">RELATED LINKS</span></span>