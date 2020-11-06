---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
ms.openlocfilehash: cb232bdebacfcb65cf3570854b14c28406d22b12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566940"
---
# <span data-ttu-id="2ed41-101">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="2ed41-101">Remove-AzureRmContext</span></span>

## <span data-ttu-id="2ed41-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ed41-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed41-103">Удаление контекста из набора доступных контекстов</span><span class="sxs-lookup"><span data-stu-id="2ed41-103">Remove a context from the set of available contexts</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ed41-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ed41-104">SYNTAX</span></span>

### <span data-ttu-id="2ed41-105">RemoveByInputObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ed41-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ed41-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="2ed41-106">RemoveByName</span></span>
```
Remove-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="2ed41-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ed41-107">DESCRIPTION</span></span>
<span data-ttu-id="2ed41-108">Удаление контекста Azure из набора контекстов</span><span class="sxs-lookup"><span data-stu-id="2ed41-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="2ed41-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ed41-109">EXAMPLES</span></span>

### <span data-ttu-id="2ed41-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2ed41-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmContext -Name Default
```

<span data-ttu-id="2ed41-111">Удалить контекст с именем по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2ed41-111">Remove the context named default</span></span>

## <span data-ttu-id="2ed41-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ed41-112">PARAMETERS</span></span>

### <span data-ttu-id="2ed41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed41-113">-DefaultProfile</span></span>
<span data-ttu-id="2ed41-114">Учетные данные, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ed41-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ed41-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2ed41-115">-Force</span></span>
<span data-ttu-id="2ed41-116">Удалить контекст даже в том случае, если это defualt</span><span class="sxs-lookup"><span data-stu-id="2ed41-116">Remove context even if it is the defualt</span></span>

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

### <span data-ttu-id="2ed41-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ed41-117">-InputObject</span></span>
<span data-ttu-id="2ed41-118">Контекстный объект, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="2ed41-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ed41-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2ed41-119">-Name</span></span>
<span data-ttu-id="2ed41-120">Имя контекста.</span><span class="sxs-lookup"><span data-stu-id="2ed41-120">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: RemoveByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed41-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ed41-121">-PassThru</span></span>
<span data-ttu-id="2ed41-122">Вернуть удаленный контекст</span><span class="sxs-lookup"><span data-stu-id="2ed41-122">Return the removed context</span></span>

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

### <span data-ttu-id="2ed41-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="2ed41-123">-Scope</span></span>
<span data-ttu-id="2ed41-124">Определяет область изменений контекста, например, применимы ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="2ed41-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed41-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ed41-125">-Confirm</span></span>
<span data-ttu-id="2ed41-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2ed41-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ed41-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ed41-127">-WhatIf</span></span>
<span data-ttu-id="2ed41-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2ed41-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ed41-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2ed41-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ed41-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed41-130">CommonParameters</span></span>
<span data-ttu-id="2ed41-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ed41-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed41-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ed41-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed41-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ed41-133">INPUTS</span></span>

### <span data-ttu-id="2ed41-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="2ed41-134">None</span></span>

## <span data-ttu-id="2ed41-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ed41-135">OUTPUTS</span></span>

### <span data-ttu-id="2ed41-136">Microsoft. Azure. Commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="2ed41-136">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="2ed41-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ed41-137">NOTES</span></span>

## <span data-ttu-id="2ed41-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ed41-138">RELATED LINKS</span></span>

