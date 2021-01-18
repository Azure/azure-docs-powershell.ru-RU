---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 25fd0e1cd651f70fa0900c528f9e5297a8eaf2df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507009"
---
# <span data-ttu-id="ceec1-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="ceec1-101">Set-AzDefault</span></span>

## <span data-ttu-id="ceec1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceec1-102">SYNOPSIS</span></span>
<span data-ttu-id="ceec1-103">Задает значение по умолчанию в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="ceec1-103">Sets a default in the current context</span></span>

## <span data-ttu-id="ceec1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ceec1-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceec1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ceec1-105">DESCRIPTION</span></span>
<span data-ttu-id="ceec1-106">Этот Set-AzDefault добавляет или изменяет значения по умолчанию в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="ceec1-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="ceec1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ceec1-107">EXAMPLES</span></span>

### <span data-ttu-id="ceec1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ceec1-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="ceec1-109">Эта команда задает для группы ресурсов по умолчанию группу ресурсов, заданную пользователем.</span><span class="sxs-lookup"><span data-stu-id="ceec1-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="ceec1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ceec1-110">PARAMETERS</span></span>

### <span data-ttu-id="ceec1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceec1-111">-DefaultProfile</span></span>
<span data-ttu-id="ceec1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ceec1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceec1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ceec1-113">-Force</span></span>
<span data-ttu-id="ceec1-114">Создание группы ресурсов, если указанное значение по умолчанию не существует</span><span class="sxs-lookup"><span data-stu-id="ceec1-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="ceec1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceec1-115">-ResourceGroupName</span></span>
<span data-ttu-id="ceec1-116">Имя группы ресурсов, за которая устанавливается по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ceec1-116">Name of the resource group being set as default</span></span>

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

### <span data-ttu-id="ceec1-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="ceec1-117">-Scope</span></span>
<span data-ttu-id="ceec1-118">Определяет область изменения контекста, например, применяются ли изменения только к текущему процессу или же к всем сеансам, на которые начал пользователь.</span><span class="sxs-lookup"><span data-stu-id="ceec1-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceec1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ceec1-119">-Confirm</span></span>
<span data-ttu-id="ceec1-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceec1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceec1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceec1-121">-WhatIf</span></span>
<span data-ttu-id="ceec1-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceec1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceec1-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ceec1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceec1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceec1-124">CommonParameters</span></span>
<span data-ttu-id="ceec1-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceec1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceec1-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceec1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceec1-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ceec1-127">INPUTS</span></span>

### <span data-ttu-id="ceec1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ceec1-128">System.String</span></span>

## <span data-ttu-id="ceec1-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ceec1-129">OUTPUTS</span></span>

### <span data-ttu-id="ceec1-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ceec1-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="ceec1-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ceec1-131">NOTES</span></span>

## <span data-ttu-id="ceec1-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ceec1-132">RELATED LINKS</span></span>
