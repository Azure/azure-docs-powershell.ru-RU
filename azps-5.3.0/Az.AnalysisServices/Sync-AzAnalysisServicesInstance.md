---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 185b152d3fe4ac4cb7d80acb6d33c408911d626d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516709"
---
# <span data-ttu-id="87914-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="87914-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="87914-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87914-102">SYNOPSIS</span></span>

<span data-ttu-id="87914-103">Синхронизация указанной базы данных в указанном экземпляре сервера Analysis Services со всеми экземплярами шкалы запроса в текущий момент в среде, как указано в Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="87914-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="87914-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="87914-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87914-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87914-105">DESCRIPTION</span></span>

<span data-ttu-id="87914-106">Командлет Sync-AzAnalysisServicesInstance синхронизирует указанную базу данных в указанном экземпляре сервера Analysis Services со всеми экземплярами шкалы запроса в текущий момент в среде, как указано в Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="87914-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="87914-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="87914-107">EXAMPLES</span></span>

### <span data-ttu-id="87914-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="87914-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="87914-109">Эта команда синхронизирует базу данных SalesOrders на сервере contoso в среде westus.asazure.windows.net если пользователь вошел в эту среду с помощью команды Add-AzAnalysisServicesAccount входа.</span><span class="sxs-lookup"><span data-stu-id="87914-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="87914-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87914-110">PARAMETERS</span></span>

### <span data-ttu-id="87914-111">-Database</span><span class="sxs-lookup"><span data-stu-id="87914-111">-Database</span></span>

<span data-ttu-id="87914-112">Удостоверение базы данных для синхронизации</span><span class="sxs-lookup"><span data-stu-id="87914-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="87914-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="87914-113">-Instance</span></span>

<span data-ttu-id="87914-114">Имя экземпляра сервера Analysis Services для перезапуска</span><span class="sxs-lookup"><span data-stu-id="87914-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="87914-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87914-115">-PassThru</span></span>

<span data-ttu-id="87914-116">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="87914-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="87914-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87914-117">-Confirm</span></span>
<span data-ttu-id="87914-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87914-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87914-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87914-119">-WhatIf</span></span>
<span data-ttu-id="87914-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87914-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87914-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="87914-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87914-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87914-122">CommonParameters</span></span>
<span data-ttu-id="87914-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87914-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87914-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87914-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87914-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87914-125">INPUTS</span></span>

### <span data-ttu-id="87914-126">System.String</span><span class="sxs-lookup"><span data-stu-id="87914-126">System.String</span></span>

## <span data-ttu-id="87914-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="87914-127">OUTPUTS</span></span>

### <span data-ttu-id="87914-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="87914-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="87914-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="87914-129">NOTES</span></span>

<span data-ttu-id="87914-130">Псевдоним: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="87914-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="87914-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87914-131">RELATED LINKS</span></span>
