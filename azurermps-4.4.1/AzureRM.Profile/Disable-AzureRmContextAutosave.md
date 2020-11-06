---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
ms.openlocfilehash: 85c3791e9947ce6f7ad2ce365239da16cec17b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568710"
---
# <span data-ttu-id="24e00-101">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="24e00-101">Disable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="24e00-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24e00-102">SYNOPSIS</span></span>
<span data-ttu-id="24e00-103">Отключите Автосохранение учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="24e00-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="24e00-104">Ваши регистрационные данные будут утрачены при следующем открытии окна PowerShell.</span><span class="sxs-lookup"><span data-stu-id="24e00-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24e00-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24e00-105">SYNTAX</span></span>

```
Disable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24e00-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24e00-106">DESCRIPTION</span></span>
<span data-ttu-id="24e00-107">Отключите Автосохранение учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="24e00-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="24e00-108">Ваши регистрационные данные будут утрачены при следующем открытии окна PowerShell.</span><span class="sxs-lookup"><span data-stu-id="24e00-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="24e00-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24e00-109">EXAMPLES</span></span>

### <span data-ttu-id="24e00-110">Отключение автосохранения контекста</span><span class="sxs-lookup"><span data-stu-id="24e00-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzureRmContextAutosave
```

<span data-ttu-id="24e00-111">Отключите Автосохранение для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="24e00-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="24e00-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24e00-112">PARAMETERS</span></span>

### <span data-ttu-id="24e00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e00-113">-DefaultProfile</span></span>
<span data-ttu-id="24e00-114">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="24e00-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24e00-115">-Scope</span><span class="sxs-lookup"><span data-stu-id="24e00-115">-Scope</span></span>
<span data-ttu-id="24e00-116">Определяет область изменений контекста, например wheher изменения применяются только к процессу cusrrent или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="24e00-116">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="24e00-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24e00-117">-Confirm</span></span>
<span data-ttu-id="24e00-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="24e00-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24e00-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24e00-119">-WhatIf</span></span>
<span data-ttu-id="24e00-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="24e00-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24e00-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="24e00-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24e00-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e00-122">CommonParameters</span></span>
<span data-ttu-id="24e00-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24e00-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e00-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24e00-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e00-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24e00-125">INPUTS</span></span>

### <span data-ttu-id="24e00-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="24e00-126">None</span></span>

## <span data-ttu-id="24e00-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24e00-127">OUTPUTS</span></span>

### <span data-ttu-id="24e00-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="24e00-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="24e00-129">Сведения о текущих параметрах автосохранения, в том числе о том, включено ли Автосохранение для текущего пользователя, а также о том, где хранятся контекстные файлы и данные.</span><span class="sxs-lookup"><span data-stu-id="24e00-129">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="24e00-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="24e00-130">NOTES</span></span>

## <span data-ttu-id="24e00-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24e00-131">RELATED LINKS</span></span>

