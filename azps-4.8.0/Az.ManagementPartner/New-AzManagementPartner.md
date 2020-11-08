---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 9e6c56fa48b71e2571b7702e170bdc3e9e41f3aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079953"
---
# <span data-ttu-id="81ab4-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="81ab4-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="81ab4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81ab4-102">SYNOPSIS</span></span>
<span data-ttu-id="81ab4-103">Связывает идентификатор сети партнера Microsoft (MPN) с текущим прошедшим проверку пользователем или участником службы.</span><span class="sxs-lookup"><span data-stu-id="81ab4-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="81ab4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81ab4-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81ab4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81ab4-105">DESCRIPTION</span></span>
<span data-ttu-id="81ab4-106">Связывает идентификатор сети партнера Microsoft (MPN) с текущим прошедшим проверку пользователем или участником службы.</span><span class="sxs-lookup"><span data-stu-id="81ab4-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="81ab4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81ab4-107">EXAMPLES</span></span>

### <span data-ttu-id="81ab4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="81ab4-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="81ab4-109">Добавление партнера по управлению</span><span class="sxs-lookup"><span data-stu-id="81ab4-109">Add a management partner</span></span>

## <span data-ttu-id="81ab4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81ab4-110">PARAMETERS</span></span>

### <span data-ttu-id="81ab4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81ab4-111">-DefaultProfile</span></span>
<span data-ttu-id="81ab4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81ab4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81ab4-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="81ab4-113">-PartnerId</span></span>
<span data-ttu-id="81ab4-114">Идентификатор партнера по управлению — номер 6 цифр.</span><span class="sxs-lookup"><span data-stu-id="81ab4-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="81ab4-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81ab4-115">-Confirm</span></span>
<span data-ttu-id="81ab4-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="81ab4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81ab4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81ab4-117">-WhatIf</span></span>
<span data-ttu-id="81ab4-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="81ab4-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81ab4-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="81ab4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81ab4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81ab4-120">CommonParameters</span></span>
<span data-ttu-id="81ab4-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81ab4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81ab4-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81ab4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81ab4-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81ab4-123">INPUTS</span></span>

### <span data-ttu-id="81ab4-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="81ab4-124">None</span></span>

## <span data-ttu-id="81ab4-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81ab4-125">OUTPUTS</span></span>

### <span data-ttu-id="81ab4-126">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="81ab4-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="81ab4-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="81ab4-127">NOTES</span></span>

## <span data-ttu-id="81ab4-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81ab4-128">RELATED LINKS</span></span>

[<span data-ttu-id="81ab4-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="81ab4-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="81ab4-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="81ab4-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="81ab4-131">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="81ab4-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)