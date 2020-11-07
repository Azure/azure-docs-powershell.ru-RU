---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: 9c9c0c3c52f610c0bb2c0198e9995cf2804b2b24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734800"
---
# <span data-ttu-id="b543c-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="b543c-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="b543c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b543c-102">SYNOPSIS</span></span>
<span data-ttu-id="b543c-103">Переименуйте контекст Azure.</span><span class="sxs-lookup"><span data-stu-id="b543c-103">Rename an Azure context.</span></span>  <span data-ttu-id="b543c-104">По умолчанию контексты названы учетной записью пользователя и подпиской.</span><span class="sxs-lookup"><span data-stu-id="b543c-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b543c-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b543c-105">SYNTAX</span></span>

### <span data-ttu-id="b543c-106">Объект input (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b543c-106">Input Object (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="b543c-107">Имя контекста</span><span class="sxs-lookup"><span data-stu-id="b543c-107">Context Name</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="b543c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b543c-108">DESCRIPTION</span></span>
<span data-ttu-id="b543c-109">Переименуйте контекст Azure.</span><span class="sxs-lookup"><span data-stu-id="b543c-109">Rename an Azure context.</span></span>  <span data-ttu-id="b543c-110">По умолчанию контексты названы учетной записью пользователя и подпиской.</span><span class="sxs-lookup"><span data-stu-id="b543c-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="b543c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b543c-111">EXAMPLES</span></span>

### <span data-ttu-id="b543c-112">Переименование контекста с помощью именованных параметров</span><span class="sxs-lookup"><span data-stu-id="b543c-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="b543c-113">Переименуйте контекст для " user1@contoso.org " с подпиской "12345-6789-2345-3567890" на "трудозатраты".</span><span class="sxs-lookup"><span data-stu-id="b543c-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="b543c-114">После этой команды вы сможете ориентироваться на контекст с помощью функции "Select-AzureRmContext Work".</span><span class="sxs-lookup"><span data-stu-id="b543c-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="b543c-115">Обратите внимание, что с помощью функции TAB можно прокручивать значения для "SourceName".</span><span class="sxs-lookup"><span data-stu-id="b543c-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="b543c-116">Переименование контекста с помощью позиционных параметров</span><span class="sxs-lookup"><span data-stu-id="b543c-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="b543c-117">Переименуйте контекст с именем "мой контекст" на "трудозатраты".</span><span class="sxs-lookup"><span data-stu-id="b543c-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="b543c-118">После этой команды вы сможете ориентироваться на контекст, используя Select-AzureRmContext трудозатраты.</span><span class="sxs-lookup"><span data-stu-id="b543c-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="b543c-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b543c-119">PARAMETERS</span></span>

### <span data-ttu-id="b543c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b543c-120">-DefaultProfile</span></span>
<span data-ttu-id="b543c-121">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b543c-121">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b543c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b543c-122">-Force</span></span>
<span data-ttu-id="b543c-123">Переименование контекста даже в том случае, если целевой контекст уже существует</span><span class="sxs-lookup"><span data-stu-id="b543c-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="b543c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b543c-124">-InputObject</span></span>
<span data-ttu-id="b543c-125">Контекстный объект, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="b543c-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Input Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b543c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b543c-126">-PassThru</span></span>
<span data-ttu-id="b543c-127">Возвращает переименованный контекст.</span><span class="sxs-lookup"><span data-stu-id="b543c-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="b543c-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="b543c-128">-Scope</span></span>
<span data-ttu-id="b543c-129">Определяет область изменений контекста, например wheher изменения применяются только к процессу cusrrent или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="b543c-129">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="b543c-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="b543c-130">-SourceName</span></span>
<span data-ttu-id="b543c-131">Имя контекста.</span><span class="sxs-lookup"><span data-stu-id="b543c-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Context Name
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b543c-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="b543c-132">-TargetName</span></span>
<span data-ttu-id="b543c-133">Новое имя контекста.</span><span class="sxs-lookup"><span data-stu-id="b543c-133">The new name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b543c-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b543c-134">-Confirm</span></span>
<span data-ttu-id="b543c-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b543c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b543c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b543c-136">-WhatIf</span></span>
<span data-ttu-id="b543c-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b543c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b543c-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b543c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b543c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b543c-139">CommonParameters</span></span>
<span data-ttu-id="b543c-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b543c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b543c-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b543c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b543c-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b543c-142">INPUTS</span></span>

### <span data-ttu-id="b543c-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="b543c-143">None</span></span>

## <span data-ttu-id="b543c-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b543c-144">OUTPUTS</span></span>

### <span data-ttu-id="b543c-145">Microsoft. Azure. Commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="b543c-145">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="b543c-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="b543c-146">NOTES</span></span>

## <span data-ttu-id="b543c-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b543c-147">RELATED LINKS</span></span>

