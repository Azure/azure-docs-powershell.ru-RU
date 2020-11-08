---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 749507ba0bc0eec8aac7600c5262533ceb02a46b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073033"
---
# <span data-ttu-id="0904b-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="0904b-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="0904b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0904b-102">SYNOPSIS</span></span>
<span data-ttu-id="0904b-103">Отключает псевдонимы префиксов AzureRm для модулей AZ.</span><span class="sxs-lookup"><span data-stu-id="0904b-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="0904b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0904b-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0904b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0904b-105">DESCRIPTION</span></span>
<span data-ttu-id="0904b-106">Отключает псевдонимы префиксов AzureRm для модулей AZ.</span><span class="sxs-lookup"><span data-stu-id="0904b-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="0904b-107">Если указан модуль-Module, в списке будут отключены псевдонимы только для перечисленных модулей.</span><span class="sxs-lookup"><span data-stu-id="0904b-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="0904b-108">В противном случае все псевдонимы AzureRm отключаются.</span><span class="sxs-lookup"><span data-stu-id="0904b-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="0904b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0904b-109">EXAMPLES</span></span>

### <span data-ttu-id="0904b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0904b-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="0904b-111">Отключение всех префиксов AzureRm для текущего сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0904b-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="0904b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0904b-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="0904b-113">Отключает AzureRm псевдонимы для модуля AZ. Accounts как для текущего процесса, так и для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="0904b-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="0904b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0904b-114">PARAMETERS</span></span>

### <span data-ttu-id="0904b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0904b-115">-DefaultProfile</span></span>
<span data-ttu-id="0904b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0904b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0904b-117">-Module</span><span class="sxs-lookup"><span data-stu-id="0904b-117">-Module</span></span>
<span data-ttu-id="0904b-118">Указывает, для каких модулей следует отключить псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="0904b-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="0904b-119">Если ничего не указано, по умолчанию используются все включенные модули.</span><span class="sxs-lookup"><span data-stu-id="0904b-119">If none are specified, default is all enabled modules.</span></span>

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

### <span data-ttu-id="0904b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0904b-120">-PassThru</span></span>
<span data-ttu-id="0904b-121">Если задано, командлет будет возвращать все отключенные псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="0904b-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="0904b-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="0904b-122">-Scope</span></span>
<span data-ttu-id="0904b-123">Указывает, какие псевдонимы областей должны быть отключены.</span><span class="sxs-lookup"><span data-stu-id="0904b-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="0904b-124">Значение по умолчанию — "процесс"</span><span class="sxs-lookup"><span data-stu-id="0904b-124">Default is 'Process'</span></span>

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

### <span data-ttu-id="0904b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0904b-125">-Confirm</span></span>
<span data-ttu-id="0904b-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0904b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0904b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0904b-127">-WhatIf</span></span>
<span data-ttu-id="0904b-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0904b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0904b-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0904b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0904b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0904b-130">CommonParameters</span></span>
<span data-ttu-id="0904b-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0904b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0904b-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0904b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0904b-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0904b-133">INPUTS</span></span>

### <span data-ttu-id="0904b-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="0904b-134">None</span></span>

## <span data-ttu-id="0904b-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0904b-135">OUTPUTS</span></span>

### <span data-ttu-id="0904b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0904b-136">System.String</span></span>

## <span data-ttu-id="0904b-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="0904b-137">NOTES</span></span>

## <span data-ttu-id="0904b-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0904b-138">RELATED LINKS</span></span>
