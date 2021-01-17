---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 193a1dab5bd08489740d0d95f65c6aad1ea85e43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327812"
---
# <span data-ttu-id="85e15-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="85e15-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="85e15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85e15-102">SYNOPSIS</span></span>
<span data-ttu-id="85e15-103">Отображение метаданных о функции автосбобоя контекста, в том числе о том, будет ли автоматически сохранен контекст и где находятся сохраненные сведения о контексте и учетных данных.</span><span class="sxs-lookup"><span data-stu-id="85e15-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="85e15-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="85e15-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85e15-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85e15-105">DESCRIPTION</span></span>
<span data-ttu-id="85e15-106">Отображение метаданных о функции автосбобоя контекста, в том числе о том, будет ли автоматически сохранен контекст и где находятся сохраненные сведения о контексте и учетных данных.</span><span class="sxs-lookup"><span data-stu-id="85e15-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="85e15-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="85e15-107">EXAMPLES</span></span>

### <span data-ttu-id="85e15-108">Получить метаданные для сохранения контекста для текущего сеанса</span><span class="sxs-lookup"><span data-stu-id="85e15-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="85e15-109">Получите сведения о том, где и где сохранен контекст.</span><span class="sxs-lookup"><span data-stu-id="85e15-109">Get details about whether and where the context is saved.</span></span>  <span data-ttu-id="85e15-110">В примере выше функция автосвета отключена.</span><span class="sxs-lookup"><span data-stu-id="85e15-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="85e15-111">Получить метаданные сохранения контекста для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="85e15-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="85e15-112">Получите подробные сведения о том, где и где сохранен контекст по умолчанию для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="85e15-112">Get details about whether and where the context is saved by default for the current user.</span></span>  <span data-ttu-id="85e15-113">Обратите внимание, что это может быть не так, как параметры, активные в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="85e15-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="85e15-114">В примере выше эта функция включена и данные сохраняются в расположении по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="85e15-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="85e15-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85e15-115">PARAMETERS</span></span>

### <span data-ttu-id="85e15-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85e15-116">-DefaultProfile</span></span>
<span data-ttu-id="85e15-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="85e15-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85e15-118">-Scope</span><span class="sxs-lookup"><span data-stu-id="85e15-118">-Scope</span></span>
<span data-ttu-id="85e15-119">Определяет область изменения контекста, например, применяются ли изменения только к текущему процессу или же к всем сеансам, на которые начал пользователь.</span><span class="sxs-lookup"><span data-stu-id="85e15-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="85e15-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e15-120">CommonParameters</span></span>
<span data-ttu-id="85e15-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85e15-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e15-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85e15-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e15-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85e15-123">INPUTS</span></span>

### <span data-ttu-id="85e15-124">Нет</span><span class="sxs-lookup"><span data-stu-id="85e15-124">None</span></span>

## <span data-ttu-id="85e15-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="85e15-125">OUTPUTS</span></span>

### <span data-ttu-id="85e15-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="85e15-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="85e15-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="85e15-127">NOTES</span></span>

## <span data-ttu-id="85e15-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85e15-128">RELATED LINKS</span></span>
