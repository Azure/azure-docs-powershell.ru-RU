---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393044
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
ms.openlocfilehash: f49ff33dbe3b7fbfd41e91140671bf61d378f1ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568498"
---
# <span data-ttu-id="453a0-101">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="453a0-101">New-AzureRmManagementPartner</span></span>

## <span data-ttu-id="453a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="453a0-102">SYNOPSIS</span></span>
<span data-ttu-id="453a0-103">Связывает идентификатор сети партнера Microsoft (MPN) с текущим прошедшим проверку пользователем или участником службы.</span><span class="sxs-lookup"><span data-stu-id="453a0-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="453a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="453a0-104">SYNTAX</span></span>

```
New-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="453a0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="453a0-105">DESCRIPTION</span></span>
<span data-ttu-id="453a0-106">Связывает идентификатор сети партнера Microsoft (MPN) с текущим прошедшим проверку пользователем или участником службы.</span><span class="sxs-lookup"><span data-stu-id="453a0-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="453a0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="453a0-107">EXAMPLES</span></span>

### <span data-ttu-id="453a0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="453a0-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="453a0-109">Добавление партнера по управлению</span><span class="sxs-lookup"><span data-stu-id="453a0-109">Add a management partner</span></span> 

## <span data-ttu-id="453a0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="453a0-110">PARAMETERS</span></span>

### <span data-ttu-id="453a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="453a0-111">-DefaultProfile</span></span>
<span data-ttu-id="453a0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="453a0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="453a0-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="453a0-113">-PartnerId</span></span>
<span data-ttu-id="453a0-114">Идентификатор партнера по управлению — номер 6 цифр.</span><span class="sxs-lookup"><span data-stu-id="453a0-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="453a0-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="453a0-115">-Confirm</span></span>
<span data-ttu-id="453a0-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="453a0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="453a0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="453a0-117">-WhatIf</span></span>
<span data-ttu-id="453a0-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="453a0-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="453a0-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="453a0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="453a0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="453a0-120">CommonParameters</span></span>
<span data-ttu-id="453a0-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="453a0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="453a0-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="453a0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="453a0-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="453a0-123">INPUTS</span></span>

### <span data-ttu-id="453a0-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="453a0-124">None</span></span>

## <span data-ttu-id="453a0-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="453a0-125">OUTPUTS</span></span>

### <span data-ttu-id="453a0-126">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="453a0-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="453a0-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="453a0-127">NOTES</span></span>

## <span data-ttu-id="453a0-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="453a0-128">RELATED LINKS</span></span>

[<span data-ttu-id="453a0-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="453a0-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="453a0-130">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="453a0-130">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="453a0-131">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="453a0-131">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
