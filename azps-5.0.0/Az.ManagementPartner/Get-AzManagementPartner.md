---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: 1031c9c8828969d16097953aa7440e2c8c0a8c1b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247329"
---
# <span data-ttu-id="45648-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="45648-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="45648-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45648-102">SYNOPSIS</span></span>
<span data-ttu-id="45648-103">Возвращает идентификатор сети партнера Microsoft (MPN) текущего пользователя или участника-службы, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="45648-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="45648-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45648-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45648-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45648-105">DESCRIPTION</span></span>
<span data-ttu-id="45648-106">Возвращает идентификатор сети партнера Microsoft (MPN) текущего пользователя или участника-службы, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="45648-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="45648-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45648-107">EXAMPLES</span></span>

### <span data-ttu-id="45648-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="45648-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="45648-109">Получение идентификатора текущего партнера по управлению</span><span class="sxs-lookup"><span data-stu-id="45648-109">Get the current management partner id</span></span>

### <span data-ttu-id="45648-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="45648-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="45648-111">Получить идентификатор текущего партнера по управлению с помощью идентификатора партнера (если они не совпадают) произойдет сбой</span><span class="sxs-lookup"><span data-stu-id="45648-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="45648-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45648-112">PARAMETERS</span></span>

### <span data-ttu-id="45648-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45648-113">-DefaultProfile</span></span>
<span data-ttu-id="45648-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45648-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45648-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="45648-115">-PartnerId</span></span>
<span data-ttu-id="45648-116">Идентификатор партнера по управлению — номер 6 цифр.</span><span class="sxs-lookup"><span data-stu-id="45648-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45648-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45648-117">CommonParameters</span></span>
<span data-ttu-id="45648-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45648-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45648-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45648-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45648-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45648-120">INPUTS</span></span>

### <span data-ttu-id="45648-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="45648-121">None</span></span>

## <span data-ttu-id="45648-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45648-122">OUTPUTS</span></span>

### <span data-ttu-id="45648-123">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="45648-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="45648-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="45648-124">NOTES</span></span>

## <span data-ttu-id="45648-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45648-125">RELATED LINKS</span></span>

[<span data-ttu-id="45648-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="45648-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="45648-127">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="45648-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="45648-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="45648-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)