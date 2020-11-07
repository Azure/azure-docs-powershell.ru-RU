---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
ms.openlocfilehash: 2147fd87cae8ef87010c54ce42dc33c85a8f6374
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720288"
---
# <span data-ttu-id="5140d-101">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="5140d-101">Disable-AzContextAutosave</span></span>

## <span data-ttu-id="5140d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5140d-102">SYNOPSIS</span></span>
<span data-ttu-id="5140d-103">Отключите Автосохранение учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="5140d-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="5140d-104">Ваши регистрационные данные будут утрачены при следующем открытии окна PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5140d-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="5140d-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5140d-105">SYNTAX</span></span>

```
Disable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5140d-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5140d-106">DESCRIPTION</span></span>
<span data-ttu-id="5140d-107">Отключите Автосохранение учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="5140d-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="5140d-108">Ваши регистрационные данные будут утрачены при следующем открытии окна PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5140d-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="5140d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5140d-109">EXAMPLES</span></span>

### <span data-ttu-id="5140d-110">Отключение автосохранения контекста</span><span class="sxs-lookup"><span data-stu-id="5140d-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzContextAutosave
```

<span data-ttu-id="5140d-111">Отключите Автосохранение для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="5140d-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="5140d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5140d-112">PARAMETERS</span></span>

### <span data-ttu-id="5140d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5140d-113">-DefaultProfile</span></span>
<span data-ttu-id="5140d-114">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5140d-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5140d-115">-Scope</span><span class="sxs-lookup"><span data-stu-id="5140d-115">-Scope</span></span>
<span data-ttu-id="5140d-116">Определяет область изменений контекста, например, применимы ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="5140d-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="5140d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5140d-117">-Confirm</span></span>
<span data-ttu-id="5140d-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5140d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5140d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5140d-119">-WhatIf</span></span>
<span data-ttu-id="5140d-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5140d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5140d-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5140d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5140d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5140d-122">CommonParameters</span></span>
<span data-ttu-id="5140d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5140d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5140d-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5140d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5140d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5140d-125">INPUTS</span></span>

### <span data-ttu-id="5140d-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="5140d-126">None</span></span>

## <span data-ttu-id="5140d-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5140d-127">OUTPUTS</span></span>

### <span data-ttu-id="5140d-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="5140d-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="5140d-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="5140d-129">NOTES</span></span>

## <span data-ttu-id="5140d-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5140d-130">RELATED LINKS</span></span>
