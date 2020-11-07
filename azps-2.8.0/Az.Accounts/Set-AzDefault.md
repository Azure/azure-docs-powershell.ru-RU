---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 6cf3c98c721b5a4f72ef63cfa5f9be991bf517ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728224"
---
# <span data-ttu-id="215fd-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="215fd-101">Set-AzDefault</span></span>

## <span data-ttu-id="215fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="215fd-102">SYNOPSIS</span></span>
<span data-ttu-id="215fd-103">Задает значение по умолчанию в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="215fd-103">Sets a default in the current context</span></span>

## <span data-ttu-id="215fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="215fd-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="215fd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="215fd-105">DESCRIPTION</span></span>
<span data-ttu-id="215fd-106">Командлет Set-AzDefault добавляет или изменяет значения по умолчанию в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="215fd-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="215fd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="215fd-107">EXAMPLES</span></span>

### <span data-ttu-id="215fd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="215fd-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="215fd-109">Эта команда задает группу ресурсов по умолчанию для группы ресурсов, заданной пользователем.</span><span class="sxs-lookup"><span data-stu-id="215fd-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="215fd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="215fd-110">PARAMETERS</span></span>

### <span data-ttu-id="215fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="215fd-111">-DefaultProfile</span></span>
<span data-ttu-id="215fd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="215fd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="215fd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="215fd-113">-Force</span></span>
<span data-ttu-id="215fd-114">Создание группы ресурсов, если указанное значение по умолчанию не существует</span><span class="sxs-lookup"><span data-stu-id="215fd-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="215fd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="215fd-115">-ResourceGroupName</span></span>
<span data-ttu-id="215fd-116">Имя группы ресурсов, заданной по умолчанию</span><span class="sxs-lookup"><span data-stu-id="215fd-116">Name of the resource group being set as default</span></span>

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

### <span data-ttu-id="215fd-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="215fd-117">-Scope</span></span>
<span data-ttu-id="215fd-118">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="215fd-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="215fd-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="215fd-119">-Confirm</span></span>
<span data-ttu-id="215fd-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="215fd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="215fd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="215fd-121">-WhatIf</span></span>
<span data-ttu-id="215fd-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="215fd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="215fd-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="215fd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="215fd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="215fd-124">CommonParameters</span></span>
<span data-ttu-id="215fd-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="215fd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="215fd-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="215fd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="215fd-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="215fd-127">INPUTS</span></span>

### <span data-ttu-id="215fd-128">System. String</span><span class="sxs-lookup"><span data-stu-id="215fd-128">System.String</span></span>

## <span data-ttu-id="215fd-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="215fd-129">OUTPUTS</span></span>

### <span data-ttu-id="215fd-130">Microsoft. Azure. Commands. Profile. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="215fd-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="215fd-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="215fd-131">NOTES</span></span>

## <span data-ttu-id="215fd-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="215fd-132">RELATED LINKS</span></span>
