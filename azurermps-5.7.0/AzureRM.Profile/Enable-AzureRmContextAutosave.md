---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/enable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
ms.openlocfilehash: 0e875087d52ecddbf216c6e49db96fefdf63e82f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567974"
---
# <span data-ttu-id="4494d-101">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="4494d-101">Enable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="4494d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4494d-102">SYNOPSIS</span></span>
<span data-ttu-id="4494d-103">Предоставление учетных данных Azure, учетной записи и сведений о подписке для сохранения и автоматической загрузки при открытии окна PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4494d-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4494d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4494d-104">SYNTAX</span></span>

```
Enable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4494d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4494d-105">DESCRIPTION</span></span>
<span data-ttu-id="4494d-106">Предоставление учетных данных Azure, учетной записи и сведений о подписке для сохранения и автоматической загрузки при открытии окна PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4494d-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="4494d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4494d-107">EXAMPLES</span></span>

### <span data-ttu-id="4494d-108">Включение учетных данных автосохранения для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="4494d-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzureRmContextAutosave
```

<span data-ttu-id="4494d-109">Включите Автосохранение учетных данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="4494d-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="4494d-110">Всякий раз, когда открывается окно PowerShell, текущий контекст сохраняется без входа.</span><span class="sxs-lookup"><span data-stu-id="4494d-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="4494d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4494d-111">PARAMETERS</span></span>

### <span data-ttu-id="4494d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4494d-112">-DefaultProfile</span></span>
<span data-ttu-id="4494d-113">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4494d-113">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4494d-114">-Scope</span><span class="sxs-lookup"><span data-stu-id="4494d-114">-Scope</span></span>
<span data-ttu-id="4494d-115">Определяет область изменений контекста, например, применимы ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="4494d-115">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="4494d-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4494d-116">-Confirm</span></span>
<span data-ttu-id="4494d-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4494d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4494d-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4494d-118">-WhatIf</span></span>
<span data-ttu-id="4494d-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4494d-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4494d-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4494d-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4494d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4494d-121">CommonParameters</span></span>
<span data-ttu-id="4494d-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4494d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4494d-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4494d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4494d-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4494d-124">INPUTS</span></span>

### <span data-ttu-id="4494d-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="4494d-125">None</span></span>

## <span data-ttu-id="4494d-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4494d-126">OUTPUTS</span></span>

### <span data-ttu-id="4494d-127">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="4494d-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="4494d-128">Сведения о текущих параметрах автосохранения, в том числе о том, включено ли Автосохранение для текущего пользователя, а также о том, где хранятся контекстные файлы и данные.</span><span class="sxs-lookup"><span data-stu-id="4494d-128">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="4494d-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="4494d-129">NOTES</span></span>

## <span data-ttu-id="4494d-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4494d-130">RELATED LINKS</span></span>

