---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
ms.openlocfilehash: 0a723400bf92569a077abc64467c3cace56da0a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420767"
---
# <span data-ttu-id="7cb12-101">Get-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="7cb12-101">Get-AzDataShareInvitation</span></span>

## <span data-ttu-id="7cb12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cb12-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb12-103">Получает приглашение на передачу данных.</span><span class="sxs-lookup"><span data-stu-id="7cb12-103">Gets information invitation of data share.</span></span>

## <span data-ttu-id="7cb12-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7cb12-104">SYNTAX</span></span>

### <span data-ttu-id="7cb12-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7cb12-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cb12-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cb12-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareInvitation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cb12-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cb12-107">DESCRIPTION</span></span>
<span data-ttu-id="7cb12-108">В **этом же проектлете Get-AzDataShareInvitation** можно получить сведения о приглашениях, добавленных в обет данных.</span><span class="sxs-lookup"><span data-stu-id="7cb12-108">The **Get-AzDataShareInvitation** cmdlet gets information on invitations added in data share.</span></span> <span data-ttu-id="7cb12-109">Если указать имя приглашения, этот cmdlet получит сведения о приглашении.</span><span class="sxs-lookup"><span data-stu-id="7cb12-109">If you specify the name of the invitation, this cmdlet gets information about the invitation.</span></span> <span data-ttu-id="7cb12-110">Если имя не указано, этот cmdlet получает сведения обо всех приглашениях в обет.</span><span class="sxs-lookup"><span data-stu-id="7cb12-110">If you do not specify a name, this cmdlet gets information about all the invitations in a share.</span></span>

## <span data-ttu-id="7cb12-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7cb12-111">EXAMPLES</span></span>

### <span data-ttu-id="7cb12-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7cb12-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation"

InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="7cb12-113">Эти команды предоставляют сведения о приглашении AdsInvitation в области обмена данными AdsShare.</span><span class="sxs-lookup"><span data-stu-id="7cb12-113">This commands provides information about invitation AdsInvitation present in data share AdsShare.</span></span>

## <span data-ttu-id="7cb12-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cb12-114">PARAMETERS</span></span>

### <span data-ttu-id="7cb12-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7cb12-115">-AccountName</span></span>
<span data-ttu-id="7cb12-116">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="7cb12-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb12-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cb12-117">-DefaultProfile</span></span>
<span data-ttu-id="7cb12-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7cb12-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cb12-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7cb12-119">-Name</span></span>
<span data-ttu-id="7cb12-120">Имя приглашения на передачу данных Azure</span><span class="sxs-lookup"><span data-stu-id="7cb12-120">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb12-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cb12-121">-ResourceGroupName</span></span>
<span data-ttu-id="7cb12-122">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="7cb12-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb12-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cb12-123">-ResourceId</span></span>
<span data-ttu-id="7cb12-124">ИД ресурса приглашения на передачу данных Azure</span><span class="sxs-lookup"><span data-stu-id="7cb12-124">The resource id of the azure data share invitation</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb12-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7cb12-125">-ShareName</span></span>
<span data-ttu-id="7cb12-126">Имя обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="7cb12-126">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb12-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb12-127">CommonParameters</span></span>
<span data-ttu-id="7cb12-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cb12-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb12-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cb12-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb12-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7cb12-130">INPUTS</span></span>

### <span data-ttu-id="7cb12-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7cb12-131">System.String</span></span>

## <span data-ttu-id="7cb12-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7cb12-132">OUTPUTS</span></span>

### <span data-ttu-id="7cb12-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="7cb12-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="7cb12-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7cb12-134">NOTES</span></span>

## <span data-ttu-id="7cb12-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7cb12-135">RELATED LINKS</span></span>
