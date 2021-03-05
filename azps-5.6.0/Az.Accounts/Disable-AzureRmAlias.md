---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 1f9f17e03a9b3cf79b2764c7711da9eee6ca104d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999074"
---
# <span data-ttu-id="3a1c1-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="3a1c1-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="3a1c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a1c1-102">SYNOPSIS</span></span>
<span data-ttu-id="3a1c1-103">Отключает псевдонимы префиксов AzureRm для модулей Az.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="3a1c1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3a1c1-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a1c1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a1c1-105">DESCRIPTION</span></span>
<span data-ttu-id="3a1c1-106">Отключает псевдонимы префиксов AzureRm для модулей Az.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="3a1c1-107">Если указан модуль -, псевдонимы будут отключены только в указанных модулях.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="3a1c1-108">В противном случае все псевдонимы AzureRm отключены.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="3a1c1-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3a1c1-109">EXAMPLES</span></span>

### <span data-ttu-id="3a1c1-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3a1c1-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="3a1c1-111">Отключает все префиксы AzureRm для текущего сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="3a1c1-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3a1c1-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="3a1c1-113">Отключает псевдонимы AzureRm для модуля Az.Accounts как для текущего процесса, так и для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="3a1c1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a1c1-114">PARAMETERS</span></span>

### <span data-ttu-id="3a1c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a1c1-115">-DefaultProfile</span></span>
<span data-ttu-id="3a1c1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a1c1-117">-Module</span><span class="sxs-lookup"><span data-stu-id="3a1c1-117">-Module</span></span>
<span data-ttu-id="3a1c1-118">Указывает, для каких модулей нужно отключить псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="3a1c1-119">Если они не указаны, по умолчанию включены все модули.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-119">If none are specified, default is all enabled modules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a1c1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a1c1-120">-PassThru</span></span>
<span data-ttu-id="3a1c1-121">При этом будет возвращены все отключенные псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="3a1c1-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="3a1c1-122">-Scope</span></span>
<span data-ttu-id="3a1c1-123">Указывает, для каких областей псевдонимы должны быть отключены.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="3a1c1-124">Значение по умолчанию — "Процесс".</span><span class="sxs-lookup"><span data-stu-id="3a1c1-124">Default is 'Process'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a1c1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a1c1-125">-Confirm</span></span>
<span data-ttu-id="3a1c1-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a1c1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a1c1-127">-WhatIf</span></span>
<span data-ttu-id="3a1c1-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a1c1-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a1c1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a1c1-130">CommonParameters</span></span>
<span data-ttu-id="3a1c1-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a1c1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a1c1-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a1c1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a1c1-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a1c1-133">INPUTS</span></span>

### <span data-ttu-id="3a1c1-134">Нет</span><span class="sxs-lookup"><span data-stu-id="3a1c1-134">None</span></span>

## <span data-ttu-id="3a1c1-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3a1c1-135">OUTPUTS</span></span>

### <span data-ttu-id="3a1c1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3a1c1-136">System.String</span></span>

## <span data-ttu-id="3a1c1-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3a1c1-137">NOTES</span></span>

## <span data-ttu-id="3a1c1-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a1c1-138">RELATED LINKS</span></span>
