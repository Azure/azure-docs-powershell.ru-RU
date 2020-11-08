---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 1be2aa8e198ae096f445b9f1972d1e0b903ae729
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243573"
---
# <span data-ttu-id="14268-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="14268-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="14268-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14268-102">SYNOPSIS</span></span>
<span data-ttu-id="14268-103">Создание центра администрирования Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="14268-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="14268-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14268-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14268-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14268-105">DESCRIPTION</span></span>
<span data-ttu-id="14268-106">Создает новое приложение центра администрирования Интернет вещей с предоставленными свойствами и метаданными.</span><span class="sxs-lookup"><span data-stu-id="14268-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="14268-107">Общие сведения о центре Интернета вещей можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="14268-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="14268-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14268-108">EXAMPLES</span></span>

### <span data-ttu-id="14268-109">Пример 1. Создайте простое центральное приложение IoT.</span><span class="sxs-lookup"><span data-stu-id="14268-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="14268-110">Пример вывода:</span><span class="sxs-lookup"><span data-stu-id="14268-110">Example Output:</span></span>

<span data-ttu-id="14268-111">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName имя: MyAppResourceName тип: Microsoft. IoTCentral/IoTApps расположение: westus тег: SKU: Microsoft. Azure., IotCentral. Models. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: MyAppResourceName поддомен: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14268-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="14268-112">Создавайте центральное приложение Интернет вещей в ST2 ценовой категории Standard, в области группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14268-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="14268-113">Пример 2. Создайте простое центральное приложение IoT.</span><span class="sxs-lookup"><span data-stu-id="14268-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="14268-114">Пример вывода:</span><span class="sxs-lookup"><span data-stu-id="14268-114">Example Output:</span></span>

<span data-ttu-id="14268-115">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName имя: MyAppResourceName тип: Microsoft. IoTCentral/IoTApps расположение: westus Tag: SKU: Microsoft. Azure. Commands. IotCentral. Models. ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My My имя домена: PSIotCentralAppSkuInfo Template: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX MyAppSubdomain: ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14268-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="14268-116">Создавайте центральное приложение IoT с помощью стандартной ценовой категории ST2 в области "westus" с настраиваемым отображаемым именем на основе шаблона IOTC-Default.</span><span class="sxs-lookup"><span data-stu-id="14268-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="14268-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14268-117">PARAMETERS</span></span>

### <span data-ttu-id="14268-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14268-118">-AsJob</span></span>
<span data-ttu-id="14268-119">Запустите командлет как задание в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="14268-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="14268-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14268-120">-DefaultProfile</span></span>
<span data-ttu-id="14268-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14268-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14268-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="14268-122">-DisplayName</span></span>
<span data-ttu-id="14268-123">Настраиваемое отображаемое имя центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="14268-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="14268-124">По умолчанию — имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="14268-124">Default is resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14268-125">-Location</span><span class="sxs-lookup"><span data-stu-id="14268-125">-Location</span></span>
<span data-ttu-id="14268-126">Расположение центрального приложения IoT.</span><span class="sxs-lookup"><span data-stu-id="14268-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="14268-127">По умолчанию — расположение целевой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14268-127">Default is the location of target resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14268-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="14268-128">-Name</span></span>
<span data-ttu-id="14268-129">Имя ресурса центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="14268-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14268-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14268-130">-ResourceGroupName</span></span>
<span data-ttu-id="14268-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14268-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14268-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="14268-132">-Sku</span></span>
<span data-ttu-id="14268-133">Ценовая категория для приложений центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="14268-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="14268-134">Значение по умолчанию — ST2.</span><span class="sxs-lookup"><span data-stu-id="14268-134">Default value is ST2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14268-135">-Поддомен</span><span class="sxs-lookup"><span data-stu-id="14268-135">-Subdomain</span></span>
<span data-ttu-id="14268-136">Поддомен для URL-адреса центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="14268-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="14268-137">Каждое приложение должно иметь уникальный поддомен.</span><span class="sxs-lookup"><span data-stu-id="14268-137">Each application must have a unique subdomain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14268-138">-Тег</span><span class="sxs-lookup"><span data-stu-id="14268-138">-Tag</span></span>
<span data-ttu-id="14268-139">Теги ресурсов центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="14268-139">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14268-140">-Template</span><span class="sxs-lookup"><span data-stu-id="14268-140">-Template</span></span>
<span data-ttu-id="14268-141">Имя шаблона приложения для центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="14268-141">IoT Central application template name.</span></span>
<span data-ttu-id="14268-142">По умолчанию — это настраиваемое приложение.</span><span class="sxs-lookup"><span data-stu-id="14268-142">Default is a custom application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14268-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14268-143">-Confirm</span></span>
<span data-ttu-id="14268-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="14268-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14268-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14268-145">-WhatIf</span></span>
<span data-ttu-id="14268-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="14268-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14268-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="14268-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14268-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14268-148">CommonParameters</span></span>
<span data-ttu-id="14268-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14268-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14268-150">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14268-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14268-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14268-151">INPUTS</span></span>

### <span data-ttu-id="14268-152">System. String</span><span class="sxs-lookup"><span data-stu-id="14268-152">System.String</span></span>

### <span data-ttu-id="14268-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="14268-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="14268-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14268-154">OUTPUTS</span></span>

### <span data-ttu-id="14268-155">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="14268-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="14268-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="14268-156">NOTES</span></span>

## <span data-ttu-id="14268-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14268-157">RELATED LINKS</span></span>
