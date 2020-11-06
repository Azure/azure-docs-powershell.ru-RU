---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
ms.openlocfilehash: 960e1b35a90b0bc1c490cbf194c20ac7a051e4d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557272"
---
# <span data-ttu-id="0f736-101">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="0f736-101">Clear-AzureRmContext</span></span>

## <span data-ttu-id="0f736-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f736-102">SYNOPSIS</span></span>
<span data-ttu-id="0f736-103">Удалите все учетные данные Azure, учетную запись и сведения о подписке.</span><span class="sxs-lookup"><span data-stu-id="0f736-103">Remove all Azure credentials, account, and subscription information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f736-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f736-104">SYNTAX</span></span>

```
Clear-AzureRmContext -Scope <ContextModificationScope> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f736-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f736-105">DESCRIPTION</span></span>
<span data-ttu-id="0f736-106">Удалите все учетные данные Azure, учетную запись и сведения о подписке.</span><span class="sxs-lookup"><span data-stu-id="0f736-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="0f736-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f736-107">EXAMPLES</span></span>

### <span data-ttu-id="0f736-108">Очистка глобального контекста</span><span class="sxs-lookup"><span data-stu-id="0f736-108">Clear global context</span></span>
```
PS C:\> Clear-AzureRmContext -Scope CurrentUser
```

<span data-ttu-id="0f736-109">Удалите все учетные записи, подписки и учетные данные для любого сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0f736-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="0f736-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f736-110">PARAMETERS</span></span>

### <span data-ttu-id="0f736-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f736-111">-DefaultProfile</span></span>
<span data-ttu-id="0f736-112">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0f736-112">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f736-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0f736-113">-Force</span></span>
<span data-ttu-id="0f736-114">Удаление всех пользователей и групп из глобальной области без запроса</span><span class="sxs-lookup"><span data-stu-id="0f736-114">Delete all users and groups from the global scope without prompting</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f736-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f736-115">-PassThru</span></span>
<span data-ttu-id="0f736-116">Возвращение значения, показывающего успешное выполнение или сбой</span><span class="sxs-lookup"><span data-stu-id="0f736-116">Return a value indicating success or failure</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f736-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="0f736-117">-Scope</span></span>
<span data-ttu-id="0f736-118">Очистите контекст только для текущего сеанса PowerShell или для всех сеансов.</span><span class="sxs-lookup"><span data-stu-id="0f736-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f736-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f736-119">-Confirm</span></span>
<span data-ttu-id="0f736-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0f736-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f736-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f736-121">-WhatIf</span></span>
<span data-ttu-id="0f736-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0f736-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f736-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0f736-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f736-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f736-124">CommonParameters</span></span>
<span data-ttu-id="0f736-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f736-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f736-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f736-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f736-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f736-127">INPUTS</span></span>

### <span data-ttu-id="0f736-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="0f736-128">None</span></span>

## <span data-ttu-id="0f736-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f736-129">OUTPUTS</span></span>

### <span data-ttu-id="0f736-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f736-130">System.Boolean</span></span>
<span data-ttu-id="0f736-131">Значение true, если контекст успешно очищен, в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="0f736-131">True if the context was successfully cleared, false otherwise.</span></span>

## <span data-ttu-id="0f736-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f736-132">NOTES</span></span>

## <span data-ttu-id="0f736-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f736-133">RELATED LINKS</span></span>

