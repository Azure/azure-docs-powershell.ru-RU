---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: b7ee3110fec96a10388ffb41b0a82647db461f37
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94245117"
---
# <span data-ttu-id="3f84e-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="3f84e-101">Clear-AzDefault</span></span>

## <span data-ttu-id="3f84e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f84e-102">SYNOPSIS</span></span>
<span data-ttu-id="3f84e-103">Очищает значения по умолчанию, заданные пользователем в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="3f84e-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="3f84e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f84e-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f84e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f84e-105">DESCRIPTION</span></span>
<span data-ttu-id="3f84e-106">Командлет Clear-AzDefault удаляет значения по умолчанию, заданные пользователем, в зависимости от параметров переключателей, указанных пользователем.</span><span class="sxs-lookup"><span data-stu-id="3f84e-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="3f84e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f84e-107">EXAMPLES</span></span>

### <span data-ttu-id="3f84e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3f84e-108">Example 1</span></span>
```powershell
PS C:\> Clear-AzDefault
```

<span data-ttu-id="3f84e-109">Эта команда удаляет все значения по умолчанию, заданные пользователем в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="3f84e-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="3f84e-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3f84e-110">Example 2</span></span>
```powershell
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="3f84e-111">Эта команда удаляет группу ресурсов по умолчанию, установленную пользователем в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="3f84e-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="3f84e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f84e-112">PARAMETERS</span></span>

### <span data-ttu-id="3f84e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f84e-113">-DefaultProfile</span></span>
<span data-ttu-id="3f84e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f84e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f84e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3f84e-115">-Force</span></span>
<span data-ttu-id="3f84e-116">Удаление всех значений по умолчанию, если не задано значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3f84e-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="3f84e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f84e-117">-PassThru</span></span>
<span data-ttu-id="3f84e-118">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="3f84e-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3f84e-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3f84e-119">-ResourceGroup</span></span>
<span data-ttu-id="3f84e-120">Очистить группу ресурсов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3f84e-120">Clear Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f84e-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="3f84e-121">-Scope</span></span>
<span data-ttu-id="3f84e-122">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="3f84e-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="3f84e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f84e-123">-Confirm</span></span>
<span data-ttu-id="3f84e-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3f84e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f84e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f84e-125">-WhatIf</span></span>
<span data-ttu-id="3f84e-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3f84e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f84e-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3f84e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f84e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f84e-128">CommonParameters</span></span>
<span data-ttu-id="3f84e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f84e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f84e-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f84e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f84e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f84e-131">INPUTS</span></span>

### <span data-ttu-id="3f84e-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3f84e-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3f84e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f84e-133">OUTPUTS</span></span>

### <span data-ttu-id="3f84e-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f84e-134">System.Boolean</span></span>

## <span data-ttu-id="3f84e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f84e-135">NOTES</span></span>

## <span data-ttu-id="3f84e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f84e-136">RELATED LINKS</span></span>
