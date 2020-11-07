---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
ms.openlocfilehash: f268c4171be78265843d5a04291bf430dc4f19b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909462"
---
# <span data-ttu-id="9ff18-101">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="9ff18-101">Disable-AzContextAutosave</span></span>

## <span data-ttu-id="9ff18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ff18-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff18-103">Отключите Автосохранение учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="9ff18-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="9ff18-104">Ваши регистрационные данные будут утрачены при следующем открытии окна PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9ff18-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="9ff18-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ff18-105">SYNTAX</span></span>

```
Disable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ff18-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ff18-106">DESCRIPTION</span></span>
<span data-ttu-id="9ff18-107">Отключите Автосохранение учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="9ff18-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="9ff18-108">Ваши регистрационные данные будут утрачены при следующем открытии окна PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9ff18-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="9ff18-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ff18-109">EXAMPLES</span></span>

### <span data-ttu-id="9ff18-110">Отключение автосохранения контекста</span><span class="sxs-lookup"><span data-stu-id="9ff18-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzContextAutosave
```

<span data-ttu-id="9ff18-111">Отключите Автосохранение для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="9ff18-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="9ff18-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ff18-112">PARAMETERS</span></span>

### <span data-ttu-id="9ff18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff18-113">-DefaultProfile</span></span>
<span data-ttu-id="9ff18-114">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9ff18-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ff18-115">-Scope</span><span class="sxs-lookup"><span data-stu-id="9ff18-115">-Scope</span></span>
<span data-ttu-id="9ff18-116">Определяет область изменений контекста, например, применимы ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="9ff18-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="9ff18-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ff18-117">-Confirm</span></span>
<span data-ttu-id="9ff18-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9ff18-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ff18-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ff18-119">-WhatIf</span></span>
<span data-ttu-id="9ff18-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9ff18-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ff18-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9ff18-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ff18-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff18-122">CommonParameters</span></span>
<span data-ttu-id="9ff18-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ff18-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff18-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ff18-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff18-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ff18-125">INPUTS</span></span>

### <span data-ttu-id="9ff18-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="9ff18-126">None</span></span>

## <span data-ttu-id="9ff18-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ff18-127">OUTPUTS</span></span>

### <span data-ttu-id="9ff18-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="9ff18-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="9ff18-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ff18-129">NOTES</span></span>

## <span data-ttu-id="9ff18-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ff18-130">RELATED LINKS</span></span>
