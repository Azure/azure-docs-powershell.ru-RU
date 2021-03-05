---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: f98a5efeece2eb1e78479c3f76de62db495c6e43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976328"
---
# <span data-ttu-id="05816-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="05816-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="05816-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05816-102">SYNOPSIS</span></span>
<span data-ttu-id="05816-103">Добавьте или обновйте один или несколько параметров "Служиная ткань" в кластер.</span><span class="sxs-lookup"><span data-stu-id="05816-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="05816-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="05816-104">SYNTAX</span></span>

### <span data-ttu-id="05816-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="05816-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05816-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="05816-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05816-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05816-107">DESCRIPTION</span></span>
<span data-ttu-id="05816-108">Используйте **Set-AzServiceFabricSetting** для добавления или обновления параметров тканью службы в кластере.</span><span class="sxs-lookup"><span data-stu-id="05816-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="05816-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="05816-109">EXAMPLES</span></span>

### <span data-ttu-id="05816-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="05816-110">Example 1</span></span>
```
Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="05816-111">Эта команда построит для maxFileOperationTimeout значение "5000" в разделе "ИменоваяСлужба".</span><span class="sxs-lookup"><span data-stu-id="05816-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>


### <span data-ttu-id="05816-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="05816-112">Example 2</span></span>
```
$fabricSettings = @(
    @{ 
        "name" = "NamingService";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "MaxFileOperationTimeout"; "Value" = "5000"  };
            @{ "Name" = "MaxOperationTimeout"; "Value" = "1200"  })
    },
    @{ 
        "name" = "Hosting";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "ActivationMaxFailureCount"; "Value" = "11"  })
    })

Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SettingsSectionDescription $fabricSettings -Verbose
```

<span data-ttu-id="05816-113">Эта команда запускает обновление для настройки нескольких параметров ткань с помощью параметра SettingsSectionDescription.</span><span class="sxs-lookup"><span data-stu-id="05816-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span></span>

## <span data-ttu-id="05816-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05816-114">PARAMETERS</span></span>

### <span data-ttu-id="05816-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05816-115">-DefaultProfile</span></span>
<span data-ttu-id="05816-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05816-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05816-117">-Name</span><span class="sxs-lookup"><span data-stu-id="05816-117">-Name</span></span>
<span data-ttu-id="05816-118">Указание имени кластера</span><span class="sxs-lookup"><span data-stu-id="05816-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="05816-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="05816-119">-Parameter</span></span>
<span data-ttu-id="05816-120">Имя параметра параметра параметра "Ткань"</span><span class="sxs-lookup"><span data-stu-id="05816-120">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="05816-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05816-121">-ResourceGroupName</span></span>
<span data-ttu-id="05816-122">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="05816-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="05816-123">-Section</span><span class="sxs-lookup"><span data-stu-id="05816-123">-Section</span></span>
<span data-ttu-id="05816-124">Имя раздела параметра "Ткань"</span><span class="sxs-lookup"><span data-stu-id="05816-124">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="05816-125">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="05816-125">-SettingsSectionDescription</span></span>
<span data-ttu-id="05816-126">Массив параметров ткань</span><span class="sxs-lookup"><span data-stu-id="05816-126">An array of fabric settings</span></span>

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

### <span data-ttu-id="05816-127">-Value</span><span class="sxs-lookup"><span data-stu-id="05816-127">-Value</span></span>
<span data-ttu-id="05816-128">Значение параметра для параметра ткань</span><span class="sxs-lookup"><span data-stu-id="05816-128">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="05816-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05816-129">-Confirm</span></span>
<span data-ttu-id="05816-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05816-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05816-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05816-131">-WhatIf</span></span>
<span data-ttu-id="05816-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05816-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05816-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="05816-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05816-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05816-134">CommonParameters</span></span>
<span data-ttu-id="05816-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05816-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05816-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05816-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05816-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05816-137">INPUTS</span></span>

### <span data-ttu-id="05816-138">System.String</span><span class="sxs-lookup"><span data-stu-id="05816-138">System.String</span></span>

### <span data-ttu-id="05816-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="05816-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="05816-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="05816-140">OUTPUTS</span></span>

### <span data-ttu-id="05816-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="05816-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="05816-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="05816-142">NOTES</span></span>

## <span data-ttu-id="05816-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05816-143">RELATED LINKS</span></span>
