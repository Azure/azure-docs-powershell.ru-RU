---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 871f3ba59fb84cea10200a7983fe7ee80b68918e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508062"
---
# <span data-ttu-id="b655d-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="b655d-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="b655d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b655d-102">SYNOPSIS</span></span>
<span data-ttu-id="b655d-103">Добавьте или обновйте один или несколько параметров "Служиная ткань" в кластер.</span><span class="sxs-lookup"><span data-stu-id="b655d-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="b655d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b655d-104">SYNTAX</span></span>

### <span data-ttu-id="b655d-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="b655d-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b655d-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="b655d-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b655d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b655d-107">DESCRIPTION</span></span>
<span data-ttu-id="b655d-108">Используйте **Set-AzServiceFabricSetting** для добавления или обновления параметров тканью службы в кластере.</span><span class="sxs-lookup"><span data-stu-id="b655d-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="b655d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b655d-109">EXAMPLES</span></span>

### <span data-ttu-id="b655d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b655d-110">Example 1</span></span>
```
Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="b655d-111">Эта команда построит для maxFileOperationTimeout значение "5000" в разделе "ИменоваяСлужба".</span><span class="sxs-lookup"><span data-stu-id="b655d-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>


### <span data-ttu-id="b655d-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b655d-112">Example 2</span></span>
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

<span data-ttu-id="b655d-113">Эта команда запускает обновление для настройки нескольких параметров ткань с помощью параметра SettingsSectionDescription.</span><span class="sxs-lookup"><span data-stu-id="b655d-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span></span>

## <span data-ttu-id="b655d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b655d-114">PARAMETERS</span></span>

### <span data-ttu-id="b655d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b655d-115">-DefaultProfile</span></span>
<span data-ttu-id="b655d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b655d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b655d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b655d-117">-Name</span></span>
<span data-ttu-id="b655d-118">Указание имени кластера</span><span class="sxs-lookup"><span data-stu-id="b655d-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="b655d-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="b655d-119">-Parameter</span></span>
<span data-ttu-id="b655d-120">Имя параметра параметра параметра "Ткань"</span><span class="sxs-lookup"><span data-stu-id="b655d-120">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="b655d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b655d-121">-ResourceGroupName</span></span>
<span data-ttu-id="b655d-122">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b655d-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b655d-123">-Section</span><span class="sxs-lookup"><span data-stu-id="b655d-123">-Section</span></span>
<span data-ttu-id="b655d-124">Имя раздела параметра "Ткань"</span><span class="sxs-lookup"><span data-stu-id="b655d-124">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="b655d-125">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="b655d-125">-SettingsSectionDescription</span></span>
<span data-ttu-id="b655d-126">Массив параметров ткань</span><span class="sxs-lookup"><span data-stu-id="b655d-126">An array of fabric settings</span></span>

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

### <span data-ttu-id="b655d-127">-Value</span><span class="sxs-lookup"><span data-stu-id="b655d-127">-Value</span></span>
<span data-ttu-id="b655d-128">Значение параметра для параметра ткань</span><span class="sxs-lookup"><span data-stu-id="b655d-128">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="b655d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b655d-129">-Confirm</span></span>
<span data-ttu-id="b655d-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b655d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b655d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b655d-131">-WhatIf</span></span>
<span data-ttu-id="b655d-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b655d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b655d-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b655d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b655d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b655d-134">CommonParameters</span></span>
<span data-ttu-id="b655d-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b655d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b655d-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b655d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b655d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b655d-137">INPUTS</span></span>

### <span data-ttu-id="b655d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b655d-138">System.String</span></span>

### <span data-ttu-id="b655d-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="b655d-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="b655d-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b655d-140">OUTPUTS</span></span>

### <span data-ttu-id="b655d-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="b655d-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b655d-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b655d-142">NOTES</span></span>

## <span data-ttu-id="b655d-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b655d-143">RELATED LINKS</span></span>
