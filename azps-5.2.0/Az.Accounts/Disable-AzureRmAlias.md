---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 749507ba0bc0eec8aac7600c5262533ceb02a46b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414959"
---
# <span data-ttu-id="af52b-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="af52b-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="af52b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af52b-102">SYNOPSIS</span></span>
<span data-ttu-id="af52b-103">Отключает псевдонимы префиксов AzureRm для модулей Az.</span><span class="sxs-lookup"><span data-stu-id="af52b-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="af52b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="af52b-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af52b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af52b-105">DESCRIPTION</span></span>
<span data-ttu-id="af52b-106">Отключает псевдонимы префиксов AzureRm для модулей Az.</span><span class="sxs-lookup"><span data-stu-id="af52b-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="af52b-107">Если указан модуль -, псевдонимы будут отключены только в указанных модулях.</span><span class="sxs-lookup"><span data-stu-id="af52b-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="af52b-108">В противном случае все псевдонимы AzureRm отключены.</span><span class="sxs-lookup"><span data-stu-id="af52b-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="af52b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="af52b-109">EXAMPLES</span></span>

### <span data-ttu-id="af52b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="af52b-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="af52b-111">Отключает все префиксы AzureRm для текущего сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="af52b-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="af52b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="af52b-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="af52b-113">Отключает псевдонимы AzureRm для модуля Az.Accounts как для текущего процесса, так и для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="af52b-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="af52b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af52b-114">PARAMETERS</span></span>

### <span data-ttu-id="af52b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af52b-115">-DefaultProfile</span></span>
<span data-ttu-id="af52b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af52b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af52b-117">-Module</span><span class="sxs-lookup"><span data-stu-id="af52b-117">-Module</span></span>
<span data-ttu-id="af52b-118">Указывает, для каких модулей нужно отключить псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="af52b-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="af52b-119">Если они не указаны, по умолчанию включены все модули.</span><span class="sxs-lookup"><span data-stu-id="af52b-119">If none are specified, default is all enabled modules.</span></span>

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

### <span data-ttu-id="af52b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af52b-120">-PassThru</span></span>
<span data-ttu-id="af52b-121">При этом будет возвращены все отключенные псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="af52b-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="af52b-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="af52b-122">-Scope</span></span>
<span data-ttu-id="af52b-123">Указывает, для каких областей псевдонимы должны быть отключены.</span><span class="sxs-lookup"><span data-stu-id="af52b-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="af52b-124">Значение по умолчанию — "Процесс".</span><span class="sxs-lookup"><span data-stu-id="af52b-124">Default is 'Process'</span></span>

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

### <span data-ttu-id="af52b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af52b-125">-Confirm</span></span>
<span data-ttu-id="af52b-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="af52b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af52b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af52b-127">-WhatIf</span></span>
<span data-ttu-id="af52b-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af52b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af52b-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="af52b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af52b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af52b-130">CommonParameters</span></span>
<span data-ttu-id="af52b-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af52b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af52b-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af52b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af52b-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af52b-133">INPUTS</span></span>

### <span data-ttu-id="af52b-134">Нет</span><span class="sxs-lookup"><span data-stu-id="af52b-134">None</span></span>

## <span data-ttu-id="af52b-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="af52b-135">OUTPUTS</span></span>

### <span data-ttu-id="af52b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="af52b-136">System.String</span></span>

## <span data-ttu-id="af52b-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="af52b-137">NOTES</span></span>

## <span data-ttu-id="af52b-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af52b-138">RELATED LINKS</span></span>
