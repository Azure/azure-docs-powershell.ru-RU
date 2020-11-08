---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: 82b5bdd7e10b8119a058ab3a30f6836ff9255d01
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079056"
---
# <span data-ttu-id="11b82-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="11b82-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="11b82-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11b82-102">SYNOPSIS</span></span>
<span data-ttu-id="11b82-103">Возвращает кэш (-ы).</span><span class="sxs-lookup"><span data-stu-id="11b82-103">Gets a cache(s).</span></span>

## <span data-ttu-id="11b82-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11b82-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11b82-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11b82-105">DESCRIPTION</span></span>
<span data-ttu-id="11b82-106">Командлет **Get-AzHpcCache** получает один кэш, кэш (ы) в определенной группе ресурсов или широкий список кэшей, подписку.</span><span class="sxs-lookup"><span data-stu-id="11b82-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="11b82-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11b82-107">EXAMPLES</span></span>

### <span data-ttu-id="11b82-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="11b82-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="11b82-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="11b82-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="11b82-110">Пример 3</span><span class="sxs-lookup"><span data-stu-id="11b82-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="11b82-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11b82-111">PARAMETERS</span></span>

### <span data-ttu-id="11b82-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b82-112">-DefaultProfile</span></span>
<span data-ttu-id="11b82-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11b82-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11b82-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="11b82-114">-Name</span></span>
<span data-ttu-id="11b82-115">Имя определенного кэша.</span><span class="sxs-lookup"><span data-stu-id="11b82-115">Name of specific cache.</span></span>

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

### <span data-ttu-id="11b82-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11b82-116">-ResourceGroupName</span></span>
<span data-ttu-id="11b82-117">Имя группы ресурсов, в которой вы хотите создать список кэшей (ов).</span><span class="sxs-lookup"><span data-stu-id="11b82-117">Name of resource group under which you want to list cache(s).</span></span>

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

### <span data-ttu-id="11b82-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b82-118">CommonParameters</span></span>
<span data-ttu-id="11b82-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11b82-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b82-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11b82-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b82-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11b82-121">INPUTS</span></span>

### <span data-ttu-id="11b82-122">System. String</span><span class="sxs-lookup"><span data-stu-id="11b82-122">System.String</span></span>

## <span data-ttu-id="11b82-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11b82-123">OUTPUTS</span></span>

### <span data-ttu-id="11b82-124">Microsoft. Azure. PowerShell. командлеты. HPCCache. Models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="11b82-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="11b82-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="11b82-125">NOTES</span></span>

## <span data-ttu-id="11b82-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11b82-126">RELATED LINKS</span></span>