---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: db4c1638d998db4f43210db4075353b108316e80
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066298"
---
# <span data-ttu-id="291cb-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="291cb-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="291cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="291cb-102">SYNOPSIS</span></span>
<span data-ttu-id="291cb-103">Создание приглашения для предоставления общего доступа.</span><span class="sxs-lookup"><span data-stu-id="291cb-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="291cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="291cb-104">SYNTAX</span></span>

### <span data-ttu-id="291cb-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="291cb-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="291cb-106">ByInvitationEmailParameterSet</span><span class="sxs-lookup"><span data-stu-id="291cb-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="291cb-107">ByInvitationTenantParameterSet</span><span class="sxs-lookup"><span data-stu-id="291cb-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="291cb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="291cb-108">DESCRIPTION</span></span>
<span data-ttu-id="291cb-109">Командлет **New-AzDataShareInvitation** отправляет приглашение целевому потребителю, используя сведения об общем доступе поставщика.</span><span class="sxs-lookup"><span data-stu-id="291cb-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="291cb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="291cb-110">EXAMPLES</span></span>

### <span data-ttu-id="291cb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="291cb-111">Example 1</span></span>
```
PS C:\> New-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation" -TargetEmail "adstest@microsoft.com"
InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/        providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="291cb-112">Эта команда создает приглашение AdsInvitation для предоставления общего доступа к AdsShare и отправляет его в целевую почту adstest@micosoft.com .</span><span class="sxs-lookup"><span data-stu-id="291cb-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@micosoft.com.</span></span>

## <span data-ttu-id="291cb-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="291cb-113">PARAMETERS</span></span>

### <span data-ttu-id="291cb-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="291cb-114">-AccountName</span></span>
<span data-ttu-id="291cb-115">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="291cb-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="291cb-116">-DefaultProfile</span></span>
<span data-ttu-id="291cb-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="291cb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="291cb-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="291cb-118">-Name</span></span>
<span data-ttu-id="291cb-119">Имя приглашения на предоставление данных Azure</span><span class="sxs-lookup"><span data-stu-id="291cb-119">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291cb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="291cb-120">-ResourceGroupName</span></span>
<span data-ttu-id="291cb-121">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="291cb-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291cb-122">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="291cb-122">-ShareName</span></span>
<span data-ttu-id="291cb-123">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="291cb-123">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291cb-124">-TargetEmail</span><span class="sxs-lookup"><span data-stu-id="291cb-124">-TargetEmail</span></span>
<span data-ttu-id="291cb-125">Идентификатор целевого объекта электронной почты</span><span class="sxs-lookup"><span data-stu-id="291cb-125">Target email id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291cb-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="291cb-126">-TargetObjectId</span></span>
<span data-ttu-id="291cb-127">Идентификатор целевого объекта</span><span class="sxs-lookup"><span data-stu-id="291cb-127">Target object id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291cb-128">-TargetTenantId</span><span class="sxs-lookup"><span data-stu-id="291cb-128">-TargetTenantId</span></span>
<span data-ttu-id="291cb-129">Идентификатор целевого клиента</span><span class="sxs-lookup"><span data-stu-id="291cb-129">Target tenant id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291cb-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="291cb-130">-Confirm</span></span>
<span data-ttu-id="291cb-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="291cb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="291cb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="291cb-132">-WhatIf</span></span>
<span data-ttu-id="291cb-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="291cb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="291cb-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="291cb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="291cb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="291cb-135">CommonParameters</span></span>
<span data-ttu-id="291cb-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="291cb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="291cb-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="291cb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="291cb-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="291cb-138">INPUTS</span></span>

### <span data-ttu-id="291cb-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="291cb-139">None</span></span>

## <span data-ttu-id="291cb-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="291cb-140">OUTPUTS</span></span>

### <span data-ttu-id="291cb-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="291cb-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="291cb-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="291cb-142">NOTES</span></span>

## <span data-ttu-id="291cb-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="291cb-143">RELATED LINKS</span></span>
