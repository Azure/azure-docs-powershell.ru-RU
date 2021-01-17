---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 939b50f6725497bb28ea333f13c04c6281f34611
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420759"
---
# <span data-ttu-id="5bc19-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="5bc19-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="5bc19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bc19-102">SYNOPSIS</span></span>
<span data-ttu-id="5bc19-103">Получает сведения о приглашениях от потребителей.</span><span class="sxs-lookup"><span data-stu-id="5bc19-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="5bc19-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5bc19-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bc19-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bc19-105">DESCRIPTION</span></span>
<span data-ttu-id="5bc19-106">**Cmdlet Get-AzDataShareceivedInvitation** предоставляет сведения обо всех приглашениях, которые получил потребитель.</span><span class="sxs-lookup"><span data-stu-id="5bc19-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="5bc19-107">Если у вас есть сведения о расположении или коде приглашения, этот cmdlet будет предоставлять сведения о приглашении в конкретном расположении или о том, где у вас есть код приглашения. В противном случае предоставляется список приглашений, отправленных потребителею.</span><span class="sxs-lookup"><span data-stu-id="5bc19-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="5bc19-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5bc19-108">EXAMPLES</span></span>

### <span data-ttu-id="5bc19-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5bc19-109">Example 1</span></span>
```
PS C:\> Get-AzDataShareReceivedInvitation -location "westus"

DataSetCount      : 3
InvitationId      : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus  : Pending
Location          : westus
RespondedAt       :
Sender            : adsprovider@microsoft.com
SenderCompanyName : ADS Test
SentAt            : 7/8/2019 10:47:10 PM
ShareName         : AdsShare
Description       : Some description
Terms             : Some terms of use
Id                : /providers/Microsoft.DataShare/consumerInvitations/167e06ff-567f-4bc7-be0c-645a6de710f3
Name              : AdsInvitation
Type              : Microsoft.DataShare/consumerInvitations
```

<span data-ttu-id="5bc19-110">Этот коммант предоставляет сведения о приглашениях от потребителей.</span><span class="sxs-lookup"><span data-stu-id="5bc19-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="5bc19-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bc19-111">PARAMETERS</span></span>

### <span data-ttu-id="5bc19-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bc19-112">-DefaultProfile</span></span>
<span data-ttu-id="5bc19-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5bc19-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bc19-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="5bc19-114">-InvitationId</span></span>
<span data-ttu-id="5bc19-115">Azure dataShare invitation id.</span><span class="sxs-lookup"><span data-stu-id="5bc19-115">Azure dataShare invitation id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc19-116">-Location</span><span class="sxs-lookup"><span data-stu-id="5bc19-116">-Location</span></span>
<span data-ttu-id="5bc19-117">Расположение приглашения для передачи данных Azure.</span><span class="sxs-lookup"><span data-stu-id="5bc19-117">Azure data share invitation location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc19-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bc19-118">CommonParameters</span></span>
<span data-ttu-id="5bc19-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bc19-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bc19-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bc19-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bc19-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bc19-121">INPUTS</span></span>

### <span data-ttu-id="5bc19-122">Нет</span><span class="sxs-lookup"><span data-stu-id="5bc19-122">None</span></span>

## <span data-ttu-id="5bc19-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5bc19-123">OUTPUTS</span></span>

### <span data-ttu-id="5bc19-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="5bc19-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="5bc19-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5bc19-125">NOTES</span></span>

## <span data-ttu-id="5bc19-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5bc19-126">RELATED LINKS</span></span>
