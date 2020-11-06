---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
ms.openlocfilehash: 60120e66596830e018351ceb492a36cd1ad1032d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565186"
---
# <span data-ttu-id="b1968-101">Get-AzureRmContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="b1968-101">Get-AzureRmContextAutosaveSetting</span></span>

## <span data-ttu-id="b1968-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1968-102">SYNOPSIS</span></span>
<span data-ttu-id="b1968-103">Отображение метаданных о функции автосохранения контекста, в том числе whterh контекст автоматически aved и там, где можно найти сохраненные сведения о контексте и учетных данных.</span><span class="sxs-lookup"><span data-stu-id="b1968-103">Display metadata about the context autosave feature, including whterh the context is automaticallys aved, and where saved context and credential information cna be found.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1968-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1968-104">SYNTAX</span></span>

```
Get-AzureRmContextAutosaveSetting [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1968-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1968-105">DESCRIPTION</span></span>
<span data-ttu-id="b1968-106">Отображение метаданных о функции автосохранения контекста, в том числе о том, сохраняется ли контекст автоматически, а также о том, где можно найти сохраненные сведения о контексте и учетных данных.</span><span class="sxs-lookup"><span data-stu-id="b1968-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="b1968-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1968-107">EXAMPLES</span></span>

### <span data-ttu-id="b1968-108">Получить контекст сохранения метаданных для текущего сеанса</span><span class="sxs-lookup"><span data-stu-id="b1968-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="b1968-109">Получение сведений о том, нужно ли сохранять и wehere контекст.</span><span class="sxs-lookup"><span data-stu-id="b1968-109">Get details about whether and wehere the context is saved.</span></span>  <span data-ttu-id="b1968-110">В приведенном выше примере функция автосохранения отключена.</span><span class="sxs-lookup"><span data-stu-id="b1968-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="b1968-111">Получение метаданных контекста для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="b1968-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="b1968-112">Получение сведений о том, сохранен ли контекст по умолчанию для текущего пользователя и wehere.</span><span class="sxs-lookup"><span data-stu-id="b1968-112">Get details about whether and wehere the context is saved by default for the current user.</span></span>  <span data-ttu-id="b1968-113">Обратите внимание, что это может отличаться от параметров, которые активны в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="b1968-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="b1968-114">В приведенном выше примере включена функция автосохранения, и данные сохраняются в папке по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b1968-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="b1968-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1968-115">PARAMETERS</span></span>

### <span data-ttu-id="b1968-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1968-116">-DefaultProfile</span></span>
<span data-ttu-id="b1968-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b1968-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1968-118">-Scope</span><span class="sxs-lookup"><span data-stu-id="b1968-118">-Scope</span></span>
<span data-ttu-id="b1968-119">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="b1968-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="b1968-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1968-120">CommonParameters</span></span>
<span data-ttu-id="b1968-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1968-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1968-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1968-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1968-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1968-123">INPUTS</span></span>

### <span data-ttu-id="b1968-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="b1968-124">None</span></span>

## <span data-ttu-id="b1968-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1968-125">OUTPUTS</span></span>

### <span data-ttu-id="b1968-126">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="b1968-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="b1968-127">Сведения о текущих параметрах автосохранения, в том числе о том, включено ли Автосохранение для текущего пользователя, а также о том, где хранятся контекстные файлы и данные.</span><span class="sxs-lookup"><span data-stu-id="b1968-127">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="b1968-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1968-128">NOTES</span></span>

## <span data-ttu-id="b1968-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1968-129">RELATED LINKS</span></span>

