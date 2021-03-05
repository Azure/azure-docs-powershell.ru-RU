---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 493f4b3e1cfaa3be59d0bd402e2c0d13dfdfad4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006691"
---
# <span data-ttu-id="0d72a-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0d72a-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="0d72a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d72a-102">SYNOPSIS</span></span>
<span data-ttu-id="0d72a-103">Обновляет идентификацию текущего пользователя или основной услуги Microsoft Partner Network(MPN).</span><span class="sxs-lookup"><span data-stu-id="0d72a-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="0d72a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0d72a-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d72a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d72a-105">DESCRIPTION</span></span>
<span data-ttu-id="0d72a-106">Обновляет идентификацию текущего пользователя или основной услуги Microsoft Partner Network(MPN).</span><span class="sxs-lookup"><span data-stu-id="0d72a-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="0d72a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0d72a-107">EXAMPLES</span></span>

### <span data-ttu-id="0d72a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0d72a-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="0d72a-109">Обновление партнера по управлению до нового партнера</span><span class="sxs-lookup"><span data-stu-id="0d72a-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="0d72a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d72a-110">PARAMETERS</span></span>

### <span data-ttu-id="0d72a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d72a-111">-DefaultProfile</span></span>
<span data-ttu-id="0d72a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d72a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d72a-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="0d72a-113">-PartnerId</span></span>
<span data-ttu-id="0d72a-114">Код партнера по управлению— это 6-значный номер.</span><span class="sxs-lookup"><span data-stu-id="0d72a-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d72a-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d72a-115">-Confirm</span></span>
<span data-ttu-id="0d72a-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0d72a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d72a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d72a-117">-WhatIf</span></span>
<span data-ttu-id="0d72a-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d72a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d72a-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0d72a-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d72a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d72a-120">CommonParameters</span></span>
<span data-ttu-id="0d72a-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d72a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d72a-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d72a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d72a-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d72a-123">INPUTS</span></span>

### <span data-ttu-id="0d72a-124">Нет</span><span class="sxs-lookup"><span data-stu-id="0d72a-124">None</span></span>

## <span data-ttu-id="0d72a-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0d72a-125">OUTPUTS</span></span>

### <span data-ttu-id="0d72a-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0d72a-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="0d72a-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0d72a-127">NOTES</span></span>

## <span data-ttu-id="0d72a-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d72a-128">RELATED LINKS</span></span>

[<span data-ttu-id="0d72a-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0d72a-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="0d72a-130">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0d72a-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="0d72a-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0d72a-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)