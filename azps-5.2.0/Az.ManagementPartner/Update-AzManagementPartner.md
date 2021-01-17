---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 326e16ff2f5bca8ca5ae987ebedf12cace87e11d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418076"
---
# <span data-ttu-id="dc8ae-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="dc8ae-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="dc8ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc8ae-102">SYNOPSIS</span></span>
<span data-ttu-id="dc8ae-103">Обновляет идентификацию текущего пользователя или основного пользователя службы Microsoft Partner Network(MPN).</span><span class="sxs-lookup"><span data-stu-id="dc8ae-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="dc8ae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dc8ae-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc8ae-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc8ae-105">DESCRIPTION</span></span>
<span data-ttu-id="dc8ae-106">Обновляет идентификацию текущего пользователя или основного пользователя службы Microsoft Partner Network(MPN).</span><span class="sxs-lookup"><span data-stu-id="dc8ae-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="dc8ae-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dc8ae-107">EXAMPLES</span></span>

### <span data-ttu-id="dc8ae-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc8ae-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="dc8ae-109">Обновление партнера по управлению до нового партнера</span><span class="sxs-lookup"><span data-stu-id="dc8ae-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="dc8ae-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc8ae-110">PARAMETERS</span></span>

### <span data-ttu-id="dc8ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc8ae-111">-DefaultProfile</span></span>
<span data-ttu-id="dc8ae-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc8ae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc8ae-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="dc8ae-113">-PartnerId</span></span>
<span data-ttu-id="dc8ae-114">Номер партнера по управлению — 6 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc8ae-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="dc8ae-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc8ae-115">-Confirm</span></span>
<span data-ttu-id="dc8ae-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc8ae-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc8ae-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc8ae-117">-WhatIf</span></span>
<span data-ttu-id="dc8ae-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc8ae-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc8ae-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dc8ae-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc8ae-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc8ae-120">CommonParameters</span></span>
<span data-ttu-id="dc8ae-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc8ae-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc8ae-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc8ae-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc8ae-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc8ae-123">INPUTS</span></span>

### <span data-ttu-id="dc8ae-124">Нет</span><span class="sxs-lookup"><span data-stu-id="dc8ae-124">None</span></span>

## <span data-ttu-id="dc8ae-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dc8ae-125">OUTPUTS</span></span>

### <span data-ttu-id="dc8ae-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="dc8ae-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="dc8ae-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dc8ae-127">NOTES</span></span>

## <span data-ttu-id="dc8ae-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc8ae-128">RELATED LINKS</span></span>

[<span data-ttu-id="dc8ae-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="dc8ae-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="dc8ae-130">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="dc8ae-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="dc8ae-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="dc8ae-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)