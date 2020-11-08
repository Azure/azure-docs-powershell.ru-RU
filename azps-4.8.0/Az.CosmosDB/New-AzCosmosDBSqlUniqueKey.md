---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244617"
---
# <span data-ttu-id="60e5c-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="60e5c-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="60e5c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60e5c-102">SYNOPSIS</span></span>
<span data-ttu-id="60e5c-103">Создает новый объект CosmosDB SQL UniqueKey.</span><span class="sxs-lookup"><span data-stu-id="60e5c-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="60e5c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60e5c-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60e5c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60e5c-105">DESCRIPTION</span></span>
<span data-ttu-id="60e5c-106">Командлет **New-AzCosmosDBSqlUniqueKey** создает новый объект типа PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="60e5c-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="60e5c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60e5c-107">EXAMPLES</span></span>

### <span data-ttu-id="60e5c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="60e5c-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="60e5c-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60e5c-109">PARAMETERS</span></span>

### <span data-ttu-id="60e5c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60e5c-110">-DefaultProfile</span></span>
<span data-ttu-id="60e5c-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60e5c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60e5c-112">-Path</span><span class="sxs-lookup"><span data-stu-id="60e5c-112">-Path</span></span>
<span data-ttu-id="60e5c-113">Массив строк со значениями пути</span><span class="sxs-lookup"><span data-stu-id="60e5c-113">Array of string of path values</span></span>

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

### <span data-ttu-id="60e5c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e5c-114">CommonParameters</span></span>
<span data-ttu-id="60e5c-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60e5c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e5c-116">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60e5c-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e5c-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60e5c-117">INPUTS</span></span>

### <span data-ttu-id="60e5c-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="60e5c-118">None</span></span>

## <span data-ttu-id="60e5c-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60e5c-119">OUTPUTS</span></span>

### <span data-ttu-id="60e5c-120">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="60e5c-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="60e5c-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="60e5c-121">NOTES</span></span>

## <span data-ttu-id="60e5c-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60e5c-122">RELATED LINKS</span></span>
