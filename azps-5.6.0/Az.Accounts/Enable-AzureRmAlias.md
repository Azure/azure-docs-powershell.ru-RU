---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: e99d7643fe67d4102e9f4eef7f9c10f131594948
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008179"
---
# <span data-ttu-id="2b709-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="2b709-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="2b709-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b709-102">SYNOPSIS</span></span>
<span data-ttu-id="2b709-103">Включает псевдонимы префиксов AzureRm для модулей Az.</span><span class="sxs-lookup"><span data-stu-id="2b709-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="2b709-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2b709-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b709-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b709-105">DESCRIPTION</span></span>
<span data-ttu-id="2b709-106">Включает псевдонимы префиксов AzureRm для модулей Az.</span><span class="sxs-lookup"><span data-stu-id="2b709-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="2b709-107">Если указан модуль -, псевдонимы включены только для указанных модулей.</span><span class="sxs-lookup"><span data-stu-id="2b709-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="2b709-108">В противном случае все псевдонимы AzureRm включены.</span><span class="sxs-lookup"><span data-stu-id="2b709-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="2b709-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2b709-109">EXAMPLES</span></span>

### <span data-ttu-id="2b709-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2b709-110">Example 1</span></span>
```powershell
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="2b709-111">Включает все префиксы AzureRm для текущего сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2b709-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="2b709-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2b709-112">Example 2</span></span>
```powershell
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="2b709-113">Включает псевдонимы AzureRm для модуля Az.Accounts как для текущего процесса, так и для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="2b709-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="2b709-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b709-114">PARAMETERS</span></span>

### <span data-ttu-id="2b709-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b709-115">-DefaultProfile</span></span>
<span data-ttu-id="2b709-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b709-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b709-117">-Module</span><span class="sxs-lookup"><span data-stu-id="2b709-117">-Module</span></span>
<span data-ttu-id="2b709-118">Указывает, для каких модулей нужно включить псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="2b709-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="2b709-119">Если они не указаны, по умолчанию заданы все модули.</span><span class="sxs-lookup"><span data-stu-id="2b709-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="2b709-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b709-120">-PassThru</span></span>
<span data-ttu-id="2b709-121">При этом будет возвращено все псевдонимы, включенные</span><span class="sxs-lookup"><span data-stu-id="2b709-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="2b709-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="2b709-122">-Scope</span></span>
<span data-ttu-id="2b709-123">Указывает, для каких областей должны быть включены псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="2b709-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="2b709-124">Значение по умолчанию — Local (Локальный).</span><span class="sxs-lookup"><span data-stu-id="2b709-124">Default is 'Local'</span></span>

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

### <span data-ttu-id="2b709-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b709-125">-Confirm</span></span>
<span data-ttu-id="2b709-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b709-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b709-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b709-127">-WhatIf</span></span>
<span data-ttu-id="2b709-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b709-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b709-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2b709-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b709-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b709-130">CommonParameters</span></span>
<span data-ttu-id="2b709-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b709-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b709-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b709-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b709-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b709-133">INPUTS</span></span>

### <span data-ttu-id="2b709-134">Нет</span><span class="sxs-lookup"><span data-stu-id="2b709-134">None</span></span>

## <span data-ttu-id="2b709-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2b709-135">OUTPUTS</span></span>

### <span data-ttu-id="2b709-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2b709-136">System.String</span></span>

## <span data-ttu-id="2b709-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2b709-137">NOTES</span></span>

## <span data-ttu-id="2b709-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b709-138">RELATED LINKS</span></span>
