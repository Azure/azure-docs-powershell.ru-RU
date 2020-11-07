---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/set-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
ms.openlocfilehash: a9b7dbc962809288979f5293c14fd875081f48bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734954"
---
# <span data-ttu-id="477d0-101">Set-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="477d0-101">Set-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="477d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="477d0-102">SYNOPSIS</span></span>
<span data-ttu-id="477d0-103">Обновляет метаданные приложения центра администрирования Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="477d0-103">Updates the metadata for an IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="477d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="477d0-104">SYNTAX</span></span>

### <span data-ttu-id="477d0-105">ResourceIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="477d0-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="477d0-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="477d0-106">InputObjectParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="477d0-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="477d0-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="477d0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="477d0-108">DESCRIPTION</span></span>
<span data-ttu-id="477d0-109">Обновите метаданные приложения центра администрирования Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="477d0-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="477d0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="477d0-110">EXAMPLES</span></span>

### <span data-ttu-id="477d0-111">Пример 1 обновление отображаемого имени</span><span class="sxs-lookup"><span data-stu-id="477d0-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="477d0-112">Обновление отображаемого имени на существующем центре администрирования Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="477d0-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="477d0-113">Пример вывода:</span><span class="sxs-lookup"><span data-stu-id="477d0-113">Example Output:</span></span>

<span data-ttu-id="477d0-114">ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/IoTApps/MyAppResourceName имя: MyAppResourceName тип: Microsoft. IoTCentral/IoTApps расположение: westus тег: SKU: Microsoft. Azure.. IotCentral. Models. ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My New Custom Display Name: PSIotCentralAppSkuInfo Template: iotc-default@1.0.0 SubscriptionId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX MyAppSubdomain: ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="477d0-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="477d0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="477d0-115">PARAMETERS</span></span>

### <span data-ttu-id="477d0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="477d0-116">-AsJob</span></span>
<span data-ttu-id="477d0-117">Запустите командлет как задание в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="477d0-117">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="477d0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="477d0-118">-DefaultProfile</span></span>
<span data-ttu-id="477d0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="477d0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d0-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="477d0-120">-DisplayName</span></span>
<span data-ttu-id="477d0-121">Настраиваемое отображаемое имя центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="477d0-121">Custom Display Name of the Iot Central Application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="477d0-122">-InputObject</span></span>
<span data-ttu-id="477d0-123">Объект ввода центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="477d0-123">Iot Central Application Input Object.</span></span>

```yaml
Type: PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="477d0-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="477d0-124">-Name</span></span>
<span data-ttu-id="477d0-125">Имя ресурса центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="477d0-125">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="477d0-126">-ResourceGroupName</span></span>
<span data-ttu-id="477d0-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="477d0-127">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="477d0-128">-ResourceId</span></span>
<span data-ttu-id="477d0-129">Идентификатор ресурса приложения центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="477d0-129">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="477d0-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="477d0-130">-Tag</span></span>
<span data-ttu-id="477d0-131">Теги ресурсов центрального приложения IOT.</span><span class="sxs-lookup"><span data-stu-id="477d0-131">Iot Central Application Resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d0-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="477d0-132">-Confirm</span></span>
<span data-ttu-id="477d0-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="477d0-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="477d0-134">-WhatIf</span></span>
<span data-ttu-id="477d0-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="477d0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="477d0-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="477d0-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477d0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="477d0-137">CommonParameters</span></span>
<span data-ttu-id="477d0-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="477d0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="477d0-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="477d0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="477d0-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="477d0-140">INPUTS</span></span>

### <span data-ttu-id="477d0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="477d0-141">System.String</span></span>
### <span data-ttu-id="477d0-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="477d0-142">System.Collections.Hashtable</span></span>
### <span data-ttu-id="477d0-143">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="477d0-143">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="477d0-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="477d0-144">OUTPUTS</span></span>

### <span data-ttu-id="477d0-145">Microsoft. Azure. Commands. IotCentral. Models. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="477d0-145">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="477d0-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="477d0-146">NOTES</span></span>

## <span data-ttu-id="477d0-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="477d0-147">RELATED LINKS</span></span>
