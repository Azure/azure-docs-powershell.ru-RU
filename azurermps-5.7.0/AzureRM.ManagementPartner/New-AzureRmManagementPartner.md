---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393044
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
ms.openlocfilehash: 9a6d6d0d21a38ac5ff41460021287e0701de6057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566974"
---
# <span data-ttu-id="62718-101">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="62718-101">New-AzureRmManagementPartner</span></span>

## <span data-ttu-id="62718-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62718-102">SYNOPSIS</span></span>
<span data-ttu-id="62718-103">Связывает идентификатор сети партнера Microsoft (MPN) с текущим прошедшим проверку пользователем или участником службы.</span><span class="sxs-lookup"><span data-stu-id="62718-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62718-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62718-104">SYNTAX</span></span>

```
New-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62718-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62718-105">DESCRIPTION</span></span>
<span data-ttu-id="62718-106">Связывает идентификатор сети партнера Microsoft (MPN) с текущим прошедшим проверку пользователем или участником службы.</span><span class="sxs-lookup"><span data-stu-id="62718-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="62718-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62718-107">EXAMPLES</span></span>

### <span data-ttu-id="62718-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62718-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="62718-109">Добавление партнера по управлению</span><span class="sxs-lookup"><span data-stu-id="62718-109">Add a management partner</span></span> 

## <span data-ttu-id="62718-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62718-110">PARAMETERS</span></span>

### <span data-ttu-id="62718-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62718-111">-DefaultProfile</span></span>
<span data-ttu-id="62718-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62718-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62718-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="62718-113">-PartnerId</span></span>
<span data-ttu-id="62718-114">Идентификатор партнера по управлению — номер 6 цифр.</span><span class="sxs-lookup"><span data-stu-id="62718-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62718-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62718-115">-Confirm</span></span>
<span data-ttu-id="62718-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="62718-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62718-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62718-117">-WhatIf</span></span>
<span data-ttu-id="62718-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="62718-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62718-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="62718-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62718-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62718-120">CommonParameters</span></span>
<span data-ttu-id="62718-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62718-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62718-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62718-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62718-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62718-123">INPUTS</span></span>

### <span data-ttu-id="62718-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="62718-124">None</span></span>

## <span data-ttu-id="62718-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62718-125">OUTPUTS</span></span>

### <span data-ttu-id="62718-126">Microsoft. Azure. Commands. Resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="62718-126">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="62718-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="62718-127">NOTES</span></span>

## <span data-ttu-id="62718-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62718-128">RELATED LINKS</span></span>

[<span data-ttu-id="62718-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="62718-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="62718-130">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="62718-130">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="62718-131">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="62718-131">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
