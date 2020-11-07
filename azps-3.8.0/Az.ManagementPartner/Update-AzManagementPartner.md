---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 326e16ff2f5bca8ca5ae987ebedf12cace87e11d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911956"
---
# <span data-ttu-id="bb4f9-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="bb4f9-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="bb4f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb4f9-102">SYNOPSIS</span></span>
<span data-ttu-id="bb4f9-103">Обновляет идентификационный номер сети партнера Майкрософт (MPN) текущего пользователя или участника-службы, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="bb4f9-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="bb4f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb4f9-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb4f9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb4f9-105">DESCRIPTION</span></span>
<span data-ttu-id="bb4f9-106">Обновляет идентификационный номер сети партнера Майкрософт (MPN) текущего пользователя или участника-службы, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="bb4f9-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="bb4f9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb4f9-107">EXAMPLES</span></span>

### <span data-ttu-id="bb4f9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bb4f9-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="bb4f9-109">Обновление партнера по управлению на новый</span><span class="sxs-lookup"><span data-stu-id="bb4f9-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="bb4f9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb4f9-110">PARAMETERS</span></span>

### <span data-ttu-id="bb4f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb4f9-111">-DefaultProfile</span></span>
<span data-ttu-id="bb4f9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb4f9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb4f9-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="bb4f9-113">-PartnerId</span></span>
<span data-ttu-id="bb4f9-114">Идентификатор партнера по управлению — номер 6 цифр.</span><span class="sxs-lookup"><span data-stu-id="bb4f9-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="bb4f9-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb4f9-115">-Confirm</span></span>
<span data-ttu-id="bb4f9-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bb4f9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb4f9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb4f9-117">-WhatIf</span></span>
<span data-ttu-id="bb4f9-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bb4f9-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb4f9-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bb4f9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb4f9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb4f9-120">CommonParameters</span></span>
<span data-ttu-id="bb4f9-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb4f9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb4f9-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb4f9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb4f9-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb4f9-123">INPUTS</span></span>

### <span data-ttu-id="bb4f9-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="bb4f9-124">None</span></span>

## <span data-ttu-id="bb4f9-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb4f9-125">OUTPUTS</span></span>

### <span data-ttu-id="bb4f9-126">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="bb4f9-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="bb4f9-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb4f9-127">NOTES</span></span>

## <span data-ttu-id="bb4f9-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb4f9-128">RELATED LINKS</span></span>

[<span data-ttu-id="bb4f9-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="bb4f9-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="bb4f9-130">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="bb4f9-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="bb4f9-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="bb4f9-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)