---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 555409187d2d48476a731be344d0404efddc946c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909421"
---
# <span data-ttu-id="a92f9-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="a92f9-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="a92f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a92f9-102">SYNOPSIS</span></span>
<span data-ttu-id="a92f9-103">Отображение метаданных о функции автосохранения контекста, в том числе о том, сохраняется ли контекст автоматически, а также о том, где можно найти сохраненные сведения о контексте и учетных данных.</span><span class="sxs-lookup"><span data-stu-id="a92f9-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="a92f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a92f9-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a92f9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a92f9-105">DESCRIPTION</span></span>
<span data-ttu-id="a92f9-106">Отображение метаданных о функции автосохранения контекста, в том числе о том, сохраняется ли контекст автоматически, а также о том, где можно найти сохраненные сведения о контексте и учетных данных.</span><span class="sxs-lookup"><span data-stu-id="a92f9-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="a92f9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a92f9-107">EXAMPLES</span></span>

### <span data-ttu-id="a92f9-108">Получить контекст сохранения метаданных для текущего сеанса</span><span class="sxs-lookup"><span data-stu-id="a92f9-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="a92f9-109">Получение сведений о том, где хранится ли контекст.</span><span class="sxs-lookup"><span data-stu-id="a92f9-109">Get details about whether and where the context is saved.</span></span>  <span data-ttu-id="a92f9-110">В приведенном выше примере функция автосохранения отключена.</span><span class="sxs-lookup"><span data-stu-id="a92f9-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="a92f9-111">Получение метаданных контекста для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="a92f9-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="a92f9-112">Получение сведений о том, как сохранить контекст по умолчанию для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="a92f9-112">Get details about whether and where the context is saved by default for the current user.</span></span>  <span data-ttu-id="a92f9-113">Обратите внимание, что это может отличаться от параметров, которые активны в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="a92f9-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="a92f9-114">В приведенном выше примере включена функция автосохранения, и данные сохраняются в папке по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a92f9-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="a92f9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a92f9-115">PARAMETERS</span></span>

### <span data-ttu-id="a92f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92f9-116">-DefaultProfile</span></span>
<span data-ttu-id="a92f9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a92f9-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a92f9-118">-Scope</span><span class="sxs-lookup"><span data-stu-id="a92f9-118">-Scope</span></span>
<span data-ttu-id="a92f9-119">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="a92f9-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="a92f9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92f9-120">CommonParameters</span></span>
<span data-ttu-id="a92f9-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a92f9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92f9-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a92f9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92f9-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a92f9-123">INPUTS</span></span>

### <span data-ttu-id="a92f9-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="a92f9-124">None</span></span>

## <span data-ttu-id="a92f9-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a92f9-125">OUTPUTS</span></span>

### <span data-ttu-id="a92f9-126">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="a92f9-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="a92f9-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="a92f9-127">NOTES</span></span>

## <span data-ttu-id="a92f9-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a92f9-128">RELATED LINKS</span></span>
