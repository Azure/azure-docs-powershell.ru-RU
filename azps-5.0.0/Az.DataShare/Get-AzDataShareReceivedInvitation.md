---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 939b50f6725497bb28ea333f13c04c6281f34611
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313037"
---
# <span data-ttu-id="bb02a-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="bb02a-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="bb02a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb02a-102">SYNOPSIS</span></span>
<span data-ttu-id="bb02a-103">Получение сведений о приглашениях для потребителей.</span><span class="sxs-lookup"><span data-stu-id="bb02a-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="bb02a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb02a-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb02a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb02a-105">DESCRIPTION</span></span>
<span data-ttu-id="bb02a-106">Командлет **Get-AzDataShareReceivedInvitation** предоставляет сведения обо всех приглашениях, которые потребитель имеет в receieved.</span><span class="sxs-lookup"><span data-stu-id="bb02a-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="bb02a-107">Если вы задаете расположение или идентификатор приглашения, этот командлет предоставляет сведения о приглашении в определенном местоположении или с указанием идентификатора приглашения. В противном случае он содержит список приглашенных, отправленных потребителю.</span><span class="sxs-lookup"><span data-stu-id="bb02a-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="bb02a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb02a-108">EXAMPLES</span></span>

### <span data-ttu-id="bb02a-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bb02a-109">Example 1</span></span>
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

<span data-ttu-id="bb02a-110">Этот канал содержит сведения о приглашениях для потребителей.</span><span class="sxs-lookup"><span data-stu-id="bb02a-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="bb02a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb02a-111">PARAMETERS</span></span>

### <span data-ttu-id="bb02a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb02a-112">-DefaultProfile</span></span>
<span data-ttu-id="bb02a-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb02a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb02a-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="bb02a-114">-InvitationId</span></span>
<span data-ttu-id="bb02a-115">Идентификатор приглашения на общий доступ к учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="bb02a-115">Azure dataShare invitation id.</span></span>

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

### <span data-ttu-id="bb02a-116">-Location</span><span class="sxs-lookup"><span data-stu-id="bb02a-116">-Location</span></span>
<span data-ttu-id="bb02a-117">Расположение приглашения на общий доступ к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="bb02a-117">Azure data share invitation location.</span></span>

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

### <span data-ttu-id="bb02a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb02a-118">CommonParameters</span></span>
<span data-ttu-id="bb02a-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb02a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb02a-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb02a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb02a-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb02a-121">INPUTS</span></span>

### <span data-ttu-id="bb02a-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="bb02a-122">None</span></span>

## <span data-ttu-id="bb02a-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb02a-123">OUTPUTS</span></span>

### <span data-ttu-id="bb02a-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="bb02a-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="bb02a-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb02a-125">NOTES</span></span>

## <span data-ttu-id="bb02a-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb02a-126">RELATED LINKS</span></span>
