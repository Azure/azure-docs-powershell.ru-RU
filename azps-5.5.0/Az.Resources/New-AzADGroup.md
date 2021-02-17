---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220521"
---
# <span data-ttu-id="e85a1-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="e85a1-101">New-AzADGroup</span></span>

## <span data-ttu-id="e85a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e85a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e85a1-103">Создает новую группу активных каталогов.</span><span class="sxs-lookup"><span data-stu-id="e85a1-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="e85a1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e85a1-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e85a1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e85a1-105">DESCRIPTION</span></span>
<span data-ttu-id="e85a1-106">Создает новую группу активных каталогов. Ниже приведены необходимые разрешения.</span><span class="sxs-lookup"><span data-stu-id="e85a1-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="e85a1-107">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="e85a1-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="e85a1-108">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e85a1-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="e85a1-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e85a1-109">Microsoft Graph</span></span>
  - <span data-ttu-id="e85a1-110">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e85a1-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="e85a1-111">PrivilegedAccess.ReadWrite.AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="e85a1-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="e85a1-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e85a1-112">EXAMPLES</span></span>

### <span data-ttu-id="e85a1-113">Пример 1. Создание группы AD</span><span class="sxs-lookup"><span data-stu-id="e85a1-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="e85a1-114">Создает новую группу AD с именем MyGroupDisplayName и псевдонимом MyGroupNick.</span><span class="sxs-lookup"><span data-stu-id="e85a1-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="e85a1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e85a1-115">PARAMETERS</span></span>

### <span data-ttu-id="e85a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e85a1-116">-DefaultProfile</span></span>
<span data-ttu-id="e85a1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e85a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e85a1-118">-Description</span><span class="sxs-lookup"><span data-stu-id="e85a1-118">-Description</span></span>
<span data-ttu-id="e85a1-119">Описание группы.</span><span class="sxs-lookup"><span data-stu-id="e85a1-119">The description for the group.</span></span>

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

### <span data-ttu-id="e85a1-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e85a1-120">-DisplayName</span></span>
<span data-ttu-id="e85a1-121">Отображаемая группа.</span><span class="sxs-lookup"><span data-stu-id="e85a1-121">The display name for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e85a1-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="e85a1-122">-MailNickname</span></span>
<span data-ttu-id="e85a1-123">Псевдоним электронной почты группы.</span><span class="sxs-lookup"><span data-stu-id="e85a1-123">The mail nickname for the group.</span></span> <span data-ttu-id="e85a1-124">Не может содержать знак @.</span><span class="sxs-lookup"><span data-stu-id="e85a1-124">Cannot contain the @ sign.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e85a1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e85a1-125">-Confirm</span></span>
<span data-ttu-id="e85a1-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e85a1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e85a1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e85a1-127">-WhatIf</span></span>
<span data-ttu-id="e85a1-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e85a1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e85a1-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e85a1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e85a1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e85a1-130">CommonParameters</span></span>
<span data-ttu-id="e85a1-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e85a1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e85a1-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e85a1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e85a1-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e85a1-133">INPUTS</span></span>

### <span data-ttu-id="e85a1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e85a1-134">System.String</span></span>

## <span data-ttu-id="e85a1-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e85a1-135">OUTPUTS</span></span>

### <span data-ttu-id="e85a1-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="e85a1-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="e85a1-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e85a1-137">NOTES</span></span>

## <span data-ttu-id="e85a1-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e85a1-138">RELATED LINKS</span></span>
