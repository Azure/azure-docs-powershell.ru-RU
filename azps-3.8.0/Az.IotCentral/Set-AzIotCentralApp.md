---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: cea582481515f519e14df9f430dc1326e72a0877
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064957"
---
# <span data-ttu-id="baf13-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="baf13-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="baf13-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="baf13-102">SYNOPSIS</span></span>
<span data-ttu-id="baf13-103">Обновляет метаданные приложения центра администрирования Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="baf13-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="baf13-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="baf13-104">SYNTAX</span></span>

### <span data-ttu-id="baf13-105">ResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="baf13-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baf13-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="baf13-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="baf13-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="baf13-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="baf13-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="baf13-108">DESCRIPTION</span></span>
<span data-ttu-id="baf13-109">Обновите метаданные приложения центра администрирования Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="baf13-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="baf13-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="baf13-110">EXAMPLES</span></span>

### <span data-ttu-id="baf13-111">Пример 1 обновление отображаемого имени</span><span class="sxs-lookup"><span data-stu-id="baf13-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="baf13-112">Обновление отображаемого имени на существующем центре администрирования Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="baf13-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="baf13-113">Пример вывода:</span><span class="sxs-lookup"><span data-stu-id="baf13-113">Example Output:</span></span>

<span data-ttu-id="baf13-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName имя: MyAppResourceName тип: Microsoft. IoTCentral/IoTApps расположение: westus тег: SKU: Microsoft. Azure.. IotCentral. Models. ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My New Custom Display Name: PSIotCentralAppSkuInfo Template: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX MyAppSubdomain: ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baf13-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="baf13-115">Пример 2 обновления поддомена</span><span class="sxs-lookup"><span data-stu-id="baf13-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="baf13-116">Обновление отображаемого имени на существующем центре администрирования Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="baf13-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="baf13-117">Пример вывода:</span><span class="sxs-lookup"><span data-stu-id="baf13-117">Example Output:</span></span>

<span data-ttu-id="baf13-118">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName имя: MyAppResourceName тип: Microsoft. IoTCentral/IoTApps расположение: westus тег: SKU: Microsoft. Azure.. IotCentral. Models..-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: Display Name поддомен: New-XXXX-XXXX-XXXX- iotc-default@1.0.0 XXXXXXXXXXXX</span><span class="sxs-lookup"><span data-stu-id="baf13-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="baf13-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="baf13-119">PARAMETERS</span></span>

### <span data-ttu-id="baf13-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="baf13-120">-AsJob</span></span>
<span data-ttu-id="baf13-121">Запустите командлет как задание в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="baf13-121">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="baf13-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf13-122">-DefaultProfile</span></span>
<span data-ttu-id="baf13-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="baf13-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baf13-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="baf13-124">-DisplayName</span></span>
<span data-ttu-id="baf13-125">Настраиваемое отображаемое имя центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="baf13-125">Custom Display Name of the Iot Central Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf13-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="baf13-126">-InputObject</span></span>
<span data-ttu-id="baf13-127">Объект ввода центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="baf13-127">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="baf13-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="baf13-128">-Name</span></span>
<span data-ttu-id="baf13-129">Имя ресурса центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="baf13-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="baf13-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baf13-130">-ResourceGroupName</span></span>
<span data-ttu-id="baf13-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="baf13-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="baf13-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="baf13-132">-ResourceId</span></span>
<span data-ttu-id="baf13-133">Идентификатор ресурса приложения центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="baf13-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="baf13-134">-Поддомен</span><span class="sxs-lookup"><span data-stu-id="baf13-134">-Subdomain</span></span>
<span data-ttu-id="baf13-135">Поддомен центрального домена для приложения Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="baf13-135">Subdomain of the IoT Central Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf13-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="baf13-136">-Tag</span></span>
<span data-ttu-id="baf13-137">Теги ресурсов центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="baf13-137">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf13-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="baf13-138">-Confirm</span></span>
<span data-ttu-id="baf13-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="baf13-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baf13-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baf13-140">-WhatIf</span></span>
<span data-ttu-id="baf13-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="baf13-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baf13-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="baf13-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baf13-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf13-143">CommonParameters</span></span>
<span data-ttu-id="baf13-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="baf13-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf13-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baf13-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf13-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="baf13-146">INPUTS</span></span>

### <span data-ttu-id="baf13-147">System. String</span><span class="sxs-lookup"><span data-stu-id="baf13-147">System.String</span></span>

### <span data-ttu-id="baf13-148">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="baf13-148">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="baf13-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="baf13-149">OUTPUTS</span></span>

### <span data-ttu-id="baf13-150">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="baf13-150">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="baf13-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="baf13-151">NOTES</span></span>

## <span data-ttu-id="baf13-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="baf13-152">RELATED LINKS</span></span>
