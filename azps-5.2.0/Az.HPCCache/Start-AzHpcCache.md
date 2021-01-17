---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 7465a74db4da777d60e097fe959ef69bed11918c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416692"
---
# <span data-ttu-id="db5bf-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="db5bf-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="db5bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db5bf-102">SYNOPSIS</span></span>
<span data-ttu-id="db5bf-103">Запускает кэш HPC.</span><span class="sxs-lookup"><span data-stu-id="db5bf-103">Starts HPC cache.</span></span>

## <span data-ttu-id="db5bf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="db5bf-104">SYNTAX</span></span>

### <span data-ttu-id="db5bf-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="db5bf-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db5bf-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5bf-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db5bf-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5bf-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db5bf-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db5bf-108">DESCRIPTION</span></span>
<span data-ttu-id="db5bf-109">Для **запуска кэша HPC запускается клиент Start-AzHpcCache.**</span><span class="sxs-lookup"><span data-stu-id="db5bf-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="db5bf-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="db5bf-110">EXAMPLES</span></span>

### <span data-ttu-id="db5bf-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="db5bf-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="db5bf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db5bf-112">PARAMETERS</span></span>

### <span data-ttu-id="db5bf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db5bf-113">-AsJob</span></span>
<span data-ttu-id="db5bf-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="db5bf-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db5bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db5bf-115">-DefaultProfile</span></span>
<span data-ttu-id="db5bf-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db5bf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db5bf-117">-Force</span><span class="sxs-lookup"><span data-stu-id="db5bf-117">-Force</span></span>
<span data-ttu-id="db5bf-118">Указывает на то, что при этом не будет предложено подтвердить запрос.</span><span class="sxs-lookup"><span data-stu-id="db5bf-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="db5bf-119">По умолчанию этот cmdlet запросит подтверждение запуска кэша.</span><span class="sxs-lookup"><span data-stu-id="db5bf-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="db5bf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db5bf-120">-InputObject</span></span>
<span data-ttu-id="db5bf-121">Объект кэша, который нужно запустить.</span><span class="sxs-lookup"><span data-stu-id="db5bf-121">The cache object to start.</span></span>

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

### <span data-ttu-id="db5bf-122">-Name</span><span class="sxs-lookup"><span data-stu-id="db5bf-122">-Name</span></span>
<span data-ttu-id="db5bf-123">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="db5bf-123">Name of cache.</span></span>

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

### <span data-ttu-id="db5bf-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db5bf-124">-PassThru</span></span>
<span data-ttu-id="db5bf-125">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="db5bf-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="db5bf-126">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="db5bf-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="db5bf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db5bf-127">-ResourceGroupName</span></span>
<span data-ttu-id="db5bf-128">Имя группы ресурсов, с которой вы хотите начать кэш.</span><span class="sxs-lookup"><span data-stu-id="db5bf-128">Name of resource group under which you want to start cache.</span></span>

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

### <span data-ttu-id="db5bf-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db5bf-129">-ResourceId</span></span>
<span data-ttu-id="db5bf-130">ИД ресурса кэша</span><span class="sxs-lookup"><span data-stu-id="db5bf-130">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db5bf-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db5bf-131">-Confirm</span></span>
<span data-ttu-id="db5bf-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db5bf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db5bf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db5bf-133">-WhatIf</span></span>
<span data-ttu-id="db5bf-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db5bf-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db5bf-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="db5bf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db5bf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db5bf-136">CommonParameters</span></span>
<span data-ttu-id="db5bf-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db5bf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db5bf-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db5bf-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db5bf-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db5bf-139">INPUTS</span></span>

### <span data-ttu-id="db5bf-140">System.String</span><span class="sxs-lookup"><span data-stu-id="db5bf-140">System.String</span></span>

## <span data-ttu-id="db5bf-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="db5bf-141">OUTPUTS</span></span>

## <span data-ttu-id="db5bf-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="db5bf-142">NOTES</span></span>

## <span data-ttu-id="db5bf-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db5bf-143">RELATED LINKS</span></span>
