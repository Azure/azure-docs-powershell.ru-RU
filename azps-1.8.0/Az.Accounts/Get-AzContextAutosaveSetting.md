---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: a6361fabaa05d99b35874ce0de388ed0fc1bdfa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720271"
---
# <span data-ttu-id="5efed-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="5efed-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="5efed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5efed-102">SYNOPSIS</span></span>
<span data-ttu-id="5efed-103">Отображение метаданных о функции автосохранения контекста, в том числе о том, сохраняется ли контекст автоматически, а также о том, где можно найти сохраненные сведения о контексте и учетных данных.</span><span class="sxs-lookup"><span data-stu-id="5efed-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="5efed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5efed-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5efed-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5efed-105">DESCRIPTION</span></span>
<span data-ttu-id="5efed-106">Отображение метаданных о функции автосохранения контекста, в том числе о том, сохраняется ли контекст автоматически, а также о том, где можно найти сохраненные сведения о контексте и учетных данных.</span><span class="sxs-lookup"><span data-stu-id="5efed-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="5efed-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5efed-107">EXAMPLES</span></span>

### <span data-ttu-id="5efed-108">Получить контекст сохранения метаданных для текущего сеанса</span><span class="sxs-lookup"><span data-stu-id="5efed-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="5efed-109">Получение сведений о том, нужно ли сохранять и wehere контекст.</span><span class="sxs-lookup"><span data-stu-id="5efed-109">Get details about whether and wehere the context is saved.</span></span>  <span data-ttu-id="5efed-110">В приведенном выше примере функция автосохранения отключена.</span><span class="sxs-lookup"><span data-stu-id="5efed-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="5efed-111">Получение метаданных контекста для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="5efed-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="5efed-112">Получение сведений о том, сохранен ли контекст по умолчанию для текущего пользователя и wehere.</span><span class="sxs-lookup"><span data-stu-id="5efed-112">Get details about whether and wehere the context is saved by default for the current user.</span></span>  <span data-ttu-id="5efed-113">Обратите внимание, что это может отличаться от параметров, которые активны в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="5efed-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="5efed-114">В приведенном выше примере включена функция автосохранения, и данные сохраняются в папке по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5efed-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="5efed-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5efed-115">PARAMETERS</span></span>

### <span data-ttu-id="5efed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5efed-116">-DefaultProfile</span></span>
<span data-ttu-id="5efed-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5efed-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5efed-118">-Scope</span><span class="sxs-lookup"><span data-stu-id="5efed-118">-Scope</span></span>
<span data-ttu-id="5efed-119">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="5efed-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="5efed-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5efed-120">CommonParameters</span></span>
<span data-ttu-id="5efed-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5efed-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5efed-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5efed-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5efed-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5efed-123">INPUTS</span></span>

### <span data-ttu-id="5efed-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="5efed-124">None</span></span>

## <span data-ttu-id="5efed-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5efed-125">OUTPUTS</span></span>

### <span data-ttu-id="5efed-126">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="5efed-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="5efed-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="5efed-127">NOTES</span></span>

## <span data-ttu-id="5efed-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5efed-128">RELATED LINKS</span></span>
