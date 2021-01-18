---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508782"
---
# <span data-ttu-id="a49e5-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="a49e5-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="a49e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a49e5-102">SYNOPSIS</span></span>
<span data-ttu-id="a49e5-103">Создание нового объекта Sql UniqueKey в SqlDb.</span><span class="sxs-lookup"><span data-stu-id="a49e5-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="a49e5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a49e5-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a49e5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a49e5-105">DESCRIPTION</span></span>
<span data-ttu-id="a49e5-106">Для создания объекта psUniqueKey нового типа создается новый объект **psCosmosDBSqlUniqueKey.**</span><span class="sxs-lookup"><span data-stu-id="a49e5-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="a49e5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a49e5-107">EXAMPLES</span></span>

### <span data-ttu-id="a49e5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a49e5-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="a49e5-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a49e5-109">PARAMETERS</span></span>

### <span data-ttu-id="a49e5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a49e5-110">-DefaultProfile</span></span>
<span data-ttu-id="a49e5-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a49e5-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49e5-112">-Path</span><span class="sxs-lookup"><span data-stu-id="a49e5-112">-Path</span></span>
<span data-ttu-id="a49e5-113">Массив значений строки пути</span><span class="sxs-lookup"><span data-stu-id="a49e5-113">Array of string of path values</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a49e5-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a49e5-114">CommonParameters</span></span>
<span data-ttu-id="a49e5-115">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a49e5-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a49e5-116">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a49e5-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a49e5-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a49e5-117">INPUTS</span></span>

### <span data-ttu-id="a49e5-118">Нет</span><span class="sxs-lookup"><span data-stu-id="a49e5-118">None</span></span>

## <span data-ttu-id="a49e5-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a49e5-119">OUTPUTS</span></span>

### <span data-ttu-id="a49e5-120">Microsoft.Azure.Commands.ЯsDB.Models.PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="a49e5-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="a49e5-121">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a49e5-121">NOTES</span></span>

## <span data-ttu-id="a49e5-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a49e5-122">RELATED LINKS</span></span>
