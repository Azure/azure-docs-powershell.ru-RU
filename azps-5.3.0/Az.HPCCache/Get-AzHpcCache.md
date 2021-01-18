---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: 82b5bdd7e10b8119a058ab3a30f6836ff9255d01
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504801"
---
# <span data-ttu-id="e465b-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="e465b-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="e465b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e465b-102">SYNOPSIS</span></span>
<span data-ttu-id="e465b-103">Кэш.</span><span class="sxs-lookup"><span data-stu-id="e465b-103">Gets a cache(s).</span></span>

## <span data-ttu-id="e465b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e465b-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e465b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e465b-105">DESCRIPTION</span></span>
<span data-ttu-id="e465b-106">Для **кэша** в определенной группе ресурсов или списка кэшов с подпиской можно получить один кэш, кэш или кэш для подписки.</span><span class="sxs-lookup"><span data-stu-id="e465b-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="e465b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e465b-107">EXAMPLES</span></span>

### <span data-ttu-id="e465b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e465b-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="e465b-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e465b-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="e465b-110">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e465b-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="e465b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e465b-111">PARAMETERS</span></span>

### <span data-ttu-id="e465b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e465b-112">-DefaultProfile</span></span>
<span data-ttu-id="e465b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e465b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e465b-114">-Name</span><span class="sxs-lookup"><span data-stu-id="e465b-114">-Name</span></span>
<span data-ttu-id="e465b-115">Имя определенного кэша.</span><span class="sxs-lookup"><span data-stu-id="e465b-115">Name of specific cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e465b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e465b-116">-ResourceGroupName</span></span>
<span data-ttu-id="e465b-117">Имя группы ресурсов, в которую вы хотите вычесть кэш.</span><span class="sxs-lookup"><span data-stu-id="e465b-117">Name of resource group under which you want to list cache(s).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e465b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e465b-118">CommonParameters</span></span>
<span data-ttu-id="e465b-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e465b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e465b-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e465b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e465b-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e465b-121">INPUTS</span></span>

### <span data-ttu-id="e465b-122">System.String</span><span class="sxs-lookup"><span data-stu-id="e465b-122">System.String</span></span>

## <span data-ttu-id="e465b-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e465b-123">OUTPUTS</span></span>

### <span data-ttu-id="e465b-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="e465b-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="e465b-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e465b-125">NOTES</span></span>

## <span data-ttu-id="e465b-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e465b-126">RELATED LINKS</span></span>
