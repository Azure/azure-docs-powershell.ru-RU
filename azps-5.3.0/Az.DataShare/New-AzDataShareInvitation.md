---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: ea042cb0db8fcb1995a935086d188efbb6c0647f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420628"
---
# <span data-ttu-id="cb92b-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="cb92b-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="cb92b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb92b-102">SYNOPSIS</span></span>
<span data-ttu-id="cb92b-103">Создает приглашение на совместное участие.</span><span class="sxs-lookup"><span data-stu-id="cb92b-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="cb92b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cb92b-104">SYNTAX</span></span>

### <span data-ttu-id="cb92b-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb92b-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb92b-106">ByInvitationEmailParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb92b-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb92b-107">ByInvitationTenantParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb92b-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb92b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb92b-108">DESCRIPTION</span></span>
<span data-ttu-id="cb92b-109">С **помощью cmdlet New-AzDataShareInvitation** целевому потребительскому поставщику отправляется приглашение со сведениями о его совместной услуге.</span><span class="sxs-lookup"><span data-stu-id="cb92b-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="cb92b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cb92b-110">EXAMPLES</span></span>

### <span data-ttu-id="cb92b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb92b-111">Example 1</span></span>
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

<span data-ttu-id="cb92b-112">Эта команда создает приглашение AdsInvitation для обмена AdsShare и отправляет его на целевой адрес электронной adstest@microsoft.com почты.</span><span class="sxs-lookup"><span data-stu-id="cb92b-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@microsoft.com.</span></span>

## <span data-ttu-id="cb92b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb92b-113">PARAMETERS</span></span>

### <span data-ttu-id="cb92b-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cb92b-114">-AccountName</span></span>
<span data-ttu-id="cb92b-115">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="cb92b-115">Azure data share account name</span></span>

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

### <span data-ttu-id="cb92b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb92b-116">-DefaultProfile</span></span>
<span data-ttu-id="cb92b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb92b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb92b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cb92b-118">-Name</span></span>
<span data-ttu-id="cb92b-119">Имя приглашения на передачу данных Azure</span><span class="sxs-lookup"><span data-stu-id="cb92b-119">Azure data share invitation name</span></span>

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

### <span data-ttu-id="cb92b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb92b-120">-ResourceGroupName</span></span>
<span data-ttu-id="cb92b-121">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="cb92b-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="cb92b-122">-ShareName</span><span class="sxs-lookup"><span data-stu-id="cb92b-122">-ShareName</span></span>
<span data-ttu-id="cb92b-123">Имя обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="cb92b-123">Azure data share name</span></span>

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

### <span data-ttu-id="cb92b-124">-Targetemail</span><span class="sxs-lookup"><span data-stu-id="cb92b-124">-TargetEmail</span></span>
<span data-ttu-id="cb92b-125">Целевой адрес электронной почты</span><span class="sxs-lookup"><span data-stu-id="cb92b-125">Target email id</span></span>

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

### <span data-ttu-id="cb92b-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="cb92b-126">-TargetObjectId</span></span>
<span data-ttu-id="cb92b-127">ИД целевого объекта</span><span class="sxs-lookup"><span data-stu-id="cb92b-127">Target object id</span></span>

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

### <span data-ttu-id="cb92b-128">-TargetTenantId</span><span class="sxs-lookup"><span data-stu-id="cb92b-128">-TargetTenantId</span></span>
<span data-ttu-id="cb92b-129">ИД целевого клиента</span><span class="sxs-lookup"><span data-stu-id="cb92b-129">Target tenant id</span></span>

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

### <span data-ttu-id="cb92b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb92b-130">-Confirm</span></span>
<span data-ttu-id="cb92b-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cb92b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb92b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb92b-132">-WhatIf</span></span>
<span data-ttu-id="cb92b-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb92b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb92b-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cb92b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb92b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb92b-135">CommonParameters</span></span>
<span data-ttu-id="cb92b-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb92b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb92b-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb92b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb92b-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb92b-138">INPUTS</span></span>

### <span data-ttu-id="cb92b-139">Нет</span><span class="sxs-lookup"><span data-stu-id="cb92b-139">None</span></span>

## <span data-ttu-id="cb92b-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb92b-140">OUTPUTS</span></span>

### <span data-ttu-id="cb92b-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="cb92b-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="cb92b-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cb92b-142">NOTES</span></span>

## <span data-ttu-id="cb92b-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb92b-143">RELATED LINKS</span></span>
