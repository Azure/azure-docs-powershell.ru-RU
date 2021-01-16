---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 185b152d3fe4ac4cb7d80acb6d33c408911d626d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401540"
---
# <span data-ttu-id="23e38-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="23e38-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="23e38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23e38-102">SYNOPSIS</span></span>

<span data-ttu-id="23e38-103">Синхронизация указанной базы данных в указанном экземпляре сервера Analysis Services со всеми экземплярами шкалы запроса в текущий момент в среде, как указано в Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="23e38-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="23e38-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="23e38-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23e38-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23e38-105">DESCRIPTION</span></span>

<span data-ttu-id="23e38-106">Командлет Sync-AzAnalysisServicesInstance синхронизирует указанную базу данных в указанном экземпляре сервера Analysis Services со всеми экземплярами шкалы запроса в текущий момент в среде, как указано в Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="23e38-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="23e38-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="23e38-107">EXAMPLES</span></span>

### <span data-ttu-id="23e38-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="23e38-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="23e38-109">Эта команда синхронизирует базу данных SalesOrders на сервере contoso в среде westus.asazure.windows.net если пользователь вошел в эту среду с помощью команды Add-AzAnalysisServicesAccount входа.</span><span class="sxs-lookup"><span data-stu-id="23e38-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="23e38-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23e38-110">PARAMETERS</span></span>

### <span data-ttu-id="23e38-111">-Database</span><span class="sxs-lookup"><span data-stu-id="23e38-111">-Database</span></span>

<span data-ttu-id="23e38-112">Удостоверение базы данных для синхронизации</span><span class="sxs-lookup"><span data-stu-id="23e38-112">Identity of the database to be synchronized</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23e38-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="23e38-113">-Instance</span></span>

<span data-ttu-id="23e38-114">Имя экземпляра сервера Analysis Services для перезапуска</span><span class="sxs-lookup"><span data-stu-id="23e38-114">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23e38-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23e38-115">-PassThru</span></span>

<span data-ttu-id="23e38-116">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="23e38-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="23e38-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23e38-117">-Confirm</span></span>
<span data-ttu-id="23e38-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="23e38-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23e38-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23e38-119">-WhatIf</span></span>
<span data-ttu-id="23e38-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23e38-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23e38-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="23e38-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23e38-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e38-122">CommonParameters</span></span>
<span data-ttu-id="23e38-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23e38-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e38-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23e38-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e38-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23e38-125">INPUTS</span></span>

### <span data-ttu-id="23e38-126">System.String</span><span class="sxs-lookup"><span data-stu-id="23e38-126">System.String</span></span>

## <span data-ttu-id="23e38-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="23e38-127">OUTPUTS</span></span>

### <span data-ttu-id="23e38-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="23e38-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="23e38-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="23e38-129">NOTES</span></span>

<span data-ttu-id="23e38-130">Псевдоним: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="23e38-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="23e38-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23e38-131">RELATED LINKS</span></span>
