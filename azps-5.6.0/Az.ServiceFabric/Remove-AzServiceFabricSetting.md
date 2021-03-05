---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: 2df7c5f6af50bf581963f08e0544eb453f4b27df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005400"
---
# <span data-ttu-id="1b0f6-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="1b0f6-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="1b0f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b0f6-102">SYNOPSIS</span></span>
<span data-ttu-id="1b0f6-103">Удалите один или несколько параметров "Служиная ткань" из кластера.</span><span class="sxs-lookup"><span data-stu-id="1b0f6-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="1b0f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1b0f6-104">SYNTAX</span></span>

### <span data-ttu-id="1b0f6-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="1b0f6-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b0f6-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="1b0f6-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b0f6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b0f6-107">DESCRIPTION</span></span>
<span data-ttu-id="1b0f6-108">Используйте **remove-AzServiceFabricSetting,** чтобы удалить параметры ткань службы из кластера.</span><span class="sxs-lookup"><span data-stu-id="1b0f6-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="1b0f6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1b0f6-109">EXAMPLES</span></span>

### <span data-ttu-id="1b0f6-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1b0f6-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="1b0f6-111">Эта команда удалит параметры MaxCursors в разделе "EseStore".</span><span class="sxs-lookup"><span data-stu-id="1b0f6-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="1b0f6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b0f6-112">PARAMETERS</span></span>

### <span data-ttu-id="1b0f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b0f6-113">-DefaultProfile</span></span>
<span data-ttu-id="1b0f6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b0f6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b0f6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1b0f6-115">-Name</span></span>
<span data-ttu-id="1b0f6-116">Указание имени кластера</span><span class="sxs-lookup"><span data-stu-id="1b0f6-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="1b0f6-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="1b0f6-117">-Parameter</span></span>
<span data-ttu-id="1b0f6-118">Имя параметра параметра параметра "Ткань"</span><span class="sxs-lookup"><span data-stu-id="1b0f6-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="1b0f6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b0f6-119">-ResourceGroupName</span></span>
<span data-ttu-id="1b0f6-120">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b0f6-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1b0f6-121">-Section</span><span class="sxs-lookup"><span data-stu-id="1b0f6-121">-Section</span></span>
<span data-ttu-id="1b0f6-122">Имя раздела параметра "Ткань"</span><span class="sxs-lookup"><span data-stu-id="1b0f6-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="1b0f6-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="1b0f6-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="1b0f6-124">Массив параметров ткань</span><span class="sxs-lookup"><span data-stu-id="1b0f6-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="1b0f6-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b0f6-125">-Confirm</span></span>
<span data-ttu-id="1b0f6-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b0f6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b0f6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b0f6-127">-WhatIf</span></span>
<span data-ttu-id="1b0f6-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b0f6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b0f6-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1b0f6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b0f6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b0f6-130">CommonParameters</span></span>
<span data-ttu-id="1b0f6-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b0f6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b0f6-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b0f6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b0f6-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b0f6-133">INPUTS</span></span>

### <span data-ttu-id="1b0f6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1b0f6-134">System.String</span></span>

### <span data-ttu-id="1b0f6-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="1b0f6-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="1b0f6-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1b0f6-136">OUTPUTS</span></span>

### <span data-ttu-id="1b0f6-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="1b0f6-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="1b0f6-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1b0f6-138">NOTES</span></span>

## <span data-ttu-id="1b0f6-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b0f6-139">RELATED LINKS</span></span>
