---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 173c78b662253bf347ad5cc30d79208ebe514c15
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909426"
---
# <span data-ttu-id="aaa82-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="aaa82-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="aaa82-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aaa82-102">SYNOPSIS</span></span>
<span data-ttu-id="aaa82-103">Включает псевдонимы префиксов AzureRm для модулей AZ.</span><span class="sxs-lookup"><span data-stu-id="aaa82-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="aaa82-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aaa82-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaa82-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaa82-105">DESCRIPTION</span></span>
<span data-ttu-id="aaa82-106">Включает псевдонимы префиксов AzureRm для модулей AZ.</span><span class="sxs-lookup"><span data-stu-id="aaa82-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="aaa82-107">Если задано-Module, для указанных модулей будут включены псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="aaa82-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="aaa82-108">В противном случае включаются все псевдонимы AzureRm.</span><span class="sxs-lookup"><span data-stu-id="aaa82-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="aaa82-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aaa82-109">EXAMPLES</span></span>

### <span data-ttu-id="aaa82-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aaa82-110">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="aaa82-111">Включает все префиксы AzureRm для текущего сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aaa82-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="aaa82-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aaa82-112">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="aaa82-113">Включает псевдонимы AzureRm для модуля AZ. Accounts для текущего процесса и для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="aaa82-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="aaa82-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aaa82-114">PARAMETERS</span></span>

### <span data-ttu-id="aaa82-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaa82-115">-DefaultProfile</span></span>
<span data-ttu-id="aaa82-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aaa82-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaa82-117">-Module</span><span class="sxs-lookup"><span data-stu-id="aaa82-117">-Module</span></span>
<span data-ttu-id="aaa82-118">Указывает, для каких модулей включать псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="aaa82-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="aaa82-119">Если ничего не указано, по умолчанию используются все модули.</span><span class="sxs-lookup"><span data-stu-id="aaa82-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="aaa82-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aaa82-120">-PassThru</span></span>
<span data-ttu-id="aaa82-121">Если задано, командлет вернет все включенные псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="aaa82-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="aaa82-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="aaa82-122">-Scope</span></span>
<span data-ttu-id="aaa82-123">Указывает, какие псевдонимы областей должны быть включены для.</span><span class="sxs-lookup"><span data-stu-id="aaa82-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="aaa82-124">По умолчанию — "Local"</span><span class="sxs-lookup"><span data-stu-id="aaa82-124">Default is 'Local'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa82-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aaa82-125">-Confirm</span></span>
<span data-ttu-id="aaa82-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aaa82-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaa82-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaa82-127">-WhatIf</span></span>
<span data-ttu-id="aaa82-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aaa82-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaa82-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aaa82-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaa82-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa82-130">CommonParameters</span></span>
<span data-ttu-id="aaa82-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aaa82-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa82-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aaa82-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa82-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aaa82-133">INPUTS</span></span>

### <span data-ttu-id="aaa82-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="aaa82-134">None</span></span>

## <span data-ttu-id="aaa82-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaa82-135">OUTPUTS</span></span>

### <span data-ttu-id="aaa82-136">System. String</span><span class="sxs-lookup"><span data-stu-id="aaa82-136">System.String</span></span>

## <span data-ttu-id="aaa82-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="aaa82-137">NOTES</span></span>

## <span data-ttu-id="aaa82-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aaa82-138">RELATED LINKS</span></span>
