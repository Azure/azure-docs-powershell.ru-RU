---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 42d643faa1b3047c6ee2e3266a68a2ce692ec676
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565352"
---
# <span data-ttu-id="45414-101">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="45414-101">Set-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="45414-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45414-102">SYNOPSIS</span></span>
<span data-ttu-id="45414-103">Добавьте или обновите один или несколько параметров структуры служб в кластере.</span><span class="sxs-lookup"><span data-stu-id="45414-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45414-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45414-104">SYNTAX</span></span>

### <span data-ttu-id="45414-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="45414-105">OneSetting</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45414-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="45414-106">BatchSettings</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45414-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45414-107">DESCRIPTION</span></span>
<span data-ttu-id="45414-108">С помощью **Set-AzureRmServiceFabricSetting** добавьте или обновите параметры структуры служб в кластере.</span><span class="sxs-lookup"><span data-stu-id="45414-108">Use **Set-AzureRmServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="45414-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45414-109">EXAMPLES</span></span>

### <span data-ttu-id="45414-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="45414-110">Example 1</span></span>
```
PS c:\> Set-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="45414-111">Эта команда присвойте параметру "MaxFileOperationTimeout" значение "5000" в разделе "NamingService".</span><span class="sxs-lookup"><span data-stu-id="45414-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="45414-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45414-112">PARAMETERS</span></span>

### <span data-ttu-id="45414-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45414-113">-DefaultProfile</span></span>
<span data-ttu-id="45414-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45414-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45414-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="45414-115">-Name</span></span>
<span data-ttu-id="45414-116">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="45414-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45414-117">-Параметр</span><span class="sxs-lookup"><span data-stu-id="45414-117">-Parameter</span></span>
<span data-ttu-id="45414-118">Параметра.</span><span class="sxs-lookup"><span data-stu-id="45414-118">Parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45414-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45414-119">-ResourceGroupName</span></span>
<span data-ttu-id="45414-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45414-120">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45414-121">-Раздел</span><span class="sxs-lookup"><span data-stu-id="45414-121">-Section</span></span>
<span data-ttu-id="45414-122">Секци.</span><span class="sxs-lookup"><span data-stu-id="45414-122">Section.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45414-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="45414-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="45414-124">Тип проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="45414-124">Client authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45414-125">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="45414-125">-Value</span></span>
<span data-ttu-id="45414-126">Значение.</span><span class="sxs-lookup"><span data-stu-id="45414-126">Value.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45414-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45414-127">-Confirm</span></span>
<span data-ttu-id="45414-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="45414-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45414-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45414-129">-WhatIf</span></span>
<span data-ttu-id="45414-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="45414-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45414-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="45414-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45414-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45414-132">CommonParameters</span></span>
<span data-ttu-id="45414-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45414-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45414-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45414-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45414-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45414-135">INPUTS</span></span>

### <span data-ttu-id="45414-136">System. String</span><span class="sxs-lookup"><span data-stu-id="45414-136">System.String</span></span>
<span data-ttu-id="45414-137">Параметры: параметр (ByValue), раздел (ByValue), значение (ByValue)</span><span class="sxs-lookup"><span data-stu-id="45414-137">Parameters: Parameter (ByValue), Section (ByValue), Value (ByValue)</span></span>

### <span data-ttu-id="45414-138">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="45414-138">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>
<span data-ttu-id="45414-139">Параметры: SettingsSectionDescription (ByValue)</span><span class="sxs-lookup"><span data-stu-id="45414-139">Parameters: SettingsSectionDescription (ByValue)</span></span>

## <span data-ttu-id="45414-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45414-140">OUTPUTS</span></span>

### <span data-ttu-id="45414-141">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="45414-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="45414-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="45414-142">NOTES</span></span>

## <span data-ttu-id="45414-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45414-143">RELATED LINKS</span></span>
