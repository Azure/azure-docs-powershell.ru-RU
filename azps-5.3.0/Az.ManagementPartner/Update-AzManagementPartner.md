---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 326e16ff2f5bca8ca5ae987ebedf12cace87e11d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508209"
---
# <span data-ttu-id="d5842-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="d5842-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="d5842-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5842-102">SYNOPSIS</span></span>
<span data-ttu-id="d5842-103">Обновляет идентификацию текущего пользователя или основного пользователя службы Microsoft Partner Network(MPN).</span><span class="sxs-lookup"><span data-stu-id="d5842-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="d5842-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d5842-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5842-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5842-105">DESCRIPTION</span></span>
<span data-ttu-id="d5842-106">Обновляет идентификацию текущего пользователя или основного пользователя службы Microsoft Partner Network(MPN).</span><span class="sxs-lookup"><span data-stu-id="d5842-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="d5842-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d5842-107">EXAMPLES</span></span>

### <span data-ttu-id="d5842-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d5842-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="d5842-109">Обновление партнера по управлению до нового партнера</span><span class="sxs-lookup"><span data-stu-id="d5842-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="d5842-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5842-110">PARAMETERS</span></span>

### <span data-ttu-id="d5842-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5842-111">-DefaultProfile</span></span>
<span data-ttu-id="d5842-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5842-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5842-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="d5842-113">-PartnerId</span></span>
<span data-ttu-id="d5842-114">Код партнера по управлению— это 6-значный номер.</span><span class="sxs-lookup"><span data-stu-id="d5842-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="d5842-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5842-115">-Confirm</span></span>
<span data-ttu-id="d5842-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d5842-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5842-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5842-117">-WhatIf</span></span>
<span data-ttu-id="d5842-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5842-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5842-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d5842-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5842-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5842-120">CommonParameters</span></span>
<span data-ttu-id="d5842-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5842-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5842-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5842-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5842-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5842-123">INPUTS</span></span>

### <span data-ttu-id="d5842-124">Нет</span><span class="sxs-lookup"><span data-stu-id="d5842-124">None</span></span>

## <span data-ttu-id="d5842-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d5842-125">OUTPUTS</span></span>

### <span data-ttu-id="d5842-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="d5842-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="d5842-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d5842-127">NOTES</span></span>

## <span data-ttu-id="d5842-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5842-128">RELATED LINKS</span></span>

[<span data-ttu-id="d5842-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="d5842-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="d5842-130">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="d5842-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="d5842-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="d5842-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)