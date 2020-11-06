---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: 510148c5d700c1378b0e468bbd5e8a9206491284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569879"
---
# <span data-ttu-id="62b4a-101">New-AzureRmOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="62b4a-101">New-AzureRmOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="62b4a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62b4a-102">SYNOPSIS</span></span>
<span data-ttu-id="62b4a-103">Определяет политику настраиваемого сбора журналов.</span><span class="sxs-lookup"><span data-stu-id="62b4a-103">Defines a custom log collection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62b4a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62b4a-104">SYNTAX</span></span>

### <span data-ttu-id="62b4a-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62b4a-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62b4a-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="62b4a-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62b4a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62b4a-107">DESCRIPTION</span></span>
<span data-ttu-id="62b4a-108">Командлет **New-AzureRmOperationalInsightsCustomLogDataSource** определяет политику настраиваемого сбора журналов.</span><span class="sxs-lookup"><span data-stu-id="62b4a-108">The **New-AzureRmOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="62b4a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62b4a-109">EXAMPLES</span></span>

## <span data-ttu-id="62b4a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62b4a-110">PARAMETERS</span></span>

### <span data-ttu-id="62b4a-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="62b4a-111">-CustomLogRawJson</span></span>
<span data-ttu-id="62b4a-112">Определяет настраиваемую политику коллекции как необработанную строку в формате JSON (объектная нотация JavaScript).</span><span class="sxs-lookup"><span data-stu-id="62b4a-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62b4a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b4a-113">-DefaultProfile</span></span>
<span data-ttu-id="62b4a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="62b4a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62b4a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="62b4a-115">-Force</span></span>
<span data-ttu-id="62b4a-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="62b4a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="62b4a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="62b4a-117">-Name</span></span>
<span data-ttu-id="62b4a-118">Задает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="62b4a-118">Specifies a name for the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62b4a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62b4a-119">-ResourceGroupName</span></span>
<span data-ttu-id="62b4a-120">Указывает имя группы ресурсов, содержащей компьютеры.</span><span class="sxs-lookup"><span data-stu-id="62b4a-120">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62b4a-121">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="62b4a-121">-Workspace</span></span>
<span data-ttu-id="62b4a-122">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="62b4a-122">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62b4a-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="62b4a-123">-WorkspaceName</span></span>
<span data-ttu-id="62b4a-124">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="62b4a-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62b4a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62b4a-125">-Confirm</span></span>
<span data-ttu-id="62b4a-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="62b4a-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b4a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62b4a-127">-WhatIf</span></span>
<span data-ttu-id="62b4a-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="62b4a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62b4a-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="62b4a-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b4a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b4a-130">CommonParameters</span></span>
<span data-ttu-id="62b4a-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62b4a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b4a-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62b4a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b4a-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62b4a-133">INPUTS</span></span>

### <span data-ttu-id="62b4a-134">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="62b4a-134">PSWorkspace</span></span>
<span data-ttu-id="62b4a-135">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="62b4a-135">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="62b4a-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62b4a-136">OUTPUTS</span></span>

### <span data-ttu-id="62b4a-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="62b4a-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="62b4a-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="62b4a-138">NOTES</span></span>

## <span data-ttu-id="62b4a-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62b4a-139">RELATED LINKS</span></span>

[<span data-ttu-id="62b4a-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="62b4a-140">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="62b4a-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="62b4a-141">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


