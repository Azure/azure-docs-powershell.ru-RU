---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 909f3be2e4a08ff1d1b0538b451ffa93f368d211
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504799"
---
# <span data-ttu-id="bedbe-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="bedbe-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="bedbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bedbe-102">SYNOPSIS</span></span>
<span data-ttu-id="bedbe-103">Обновляет теги в кэше HPC.</span><span class="sxs-lookup"><span data-stu-id="bedbe-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="bedbe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bedbe-104">SYNTAX</span></span>

### <span data-ttu-id="bedbe-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bedbe-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bedbe-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bedbe-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bedbe-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bedbe-107">DESCRIPTION</span></span>
<span data-ttu-id="bedbe-108">Командлет **Set-AzHpcCache** обновляет теги кэша HPC Azure.</span><span class="sxs-lookup"><span data-stu-id="bedbe-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="bedbe-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bedbe-109">EXAMPLES</span></span>

### <span data-ttu-id="bedbe-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bedbe-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="bedbe-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bedbe-111">PARAMETERS</span></span>

### <span data-ttu-id="bedbe-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bedbe-112">-AsJob</span></span>
<span data-ttu-id="bedbe-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bedbe-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bedbe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bedbe-114">-DefaultProfile</span></span>
<span data-ttu-id="bedbe-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bedbe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bedbe-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bedbe-116">-InputObject</span></span>
<span data-ttu-id="bedbe-117">Обновляемый объект кэша.</span><span class="sxs-lookup"><span data-stu-id="bedbe-117">The cache object to update.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bedbe-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bedbe-118">-Name</span></span>
<span data-ttu-id="bedbe-119">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="bedbe-119">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bedbe-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bedbe-120">-ResourceGroupName</span></span>
<span data-ttu-id="bedbe-121">Имя группы ресурсов, под которой вы хотите обновить кэш.</span><span class="sxs-lookup"><span data-stu-id="bedbe-121">Name of resource group under which you want to update cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bedbe-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="bedbe-122">-Tag</span></span>
<span data-ttu-id="bedbe-123">Теги, которые нужно связать с кэшом HPC.</span><span class="sxs-lookup"><span data-stu-id="bedbe-123">The tags to associate with HPC Cache.</span></span> 

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bedbe-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bedbe-124">-Confirm</span></span>
<span data-ttu-id="bedbe-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bedbe-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bedbe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bedbe-126">-WhatIf</span></span>
<span data-ttu-id="bedbe-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bedbe-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bedbe-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bedbe-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bedbe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bedbe-129">CommonParameters</span></span>
<span data-ttu-id="bedbe-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bedbe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bedbe-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bedbe-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bedbe-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bedbe-132">INPUTS</span></span>

### <span data-ttu-id="bedbe-133">System.String</span><span class="sxs-lookup"><span data-stu-id="bedbe-133">System.String</span></span>

### <span data-ttu-id="bedbe-134">System.Int32</span><span class="sxs-lookup"><span data-stu-id="bedbe-134">System.Int32</span></span>

## <span data-ttu-id="bedbe-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bedbe-135">OUTPUTS</span></span>

### <span data-ttu-id="bedbe-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="bedbe-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="bedbe-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bedbe-137">NOTES</span></span>

## <span data-ttu-id="bedbe-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bedbe-138">RELATED LINKS</span></span>
