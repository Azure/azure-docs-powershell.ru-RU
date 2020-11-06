---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/get-azurermmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
ms.openlocfilehash: b1fe94533074860a3c95c05d6609bb8ebb446a9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565499"
---
# <span data-ttu-id="8d823-101">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8d823-101">Get-AzureRmManagementPartner</span></span>

## <span data-ttu-id="8d823-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d823-102">SYNOPSIS</span></span>
<span data-ttu-id="8d823-103">Возвращает идентификатор сети партнера Microsoft (MPN) текущего пользователя или участника-службы, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="8d823-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d823-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d823-104">SYNTAX</span></span>

```
Get-AzureRmManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d823-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d823-105">DESCRIPTION</span></span>
<span data-ttu-id="8d823-106">Возвращает идентификатор сети партнера Microsoft (MPN) текущего пользователя или участника-службы, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="8d823-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span> 

## <span data-ttu-id="8d823-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d823-107">EXAMPLES</span></span>

### <span data-ttu-id="8d823-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8d823-108">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="8d823-109">Получение идентификатора текущего партнера по управлению</span><span class="sxs-lookup"><span data-stu-id="8d823-109">Get the current management partner id</span></span>

### <span data-ttu-id="8d823-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8d823-110">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="8d823-111">Получить идентификатор текущего партнера по управлению с помощью идентификатора партнера (если они не совпадают) произойдет сбой</span><span class="sxs-lookup"><span data-stu-id="8d823-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="8d823-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d823-112">PARAMETERS</span></span>

### <span data-ttu-id="8d823-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d823-113">-DefaultProfile</span></span>
<span data-ttu-id="8d823-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d823-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d823-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="8d823-115">-PartnerId</span></span>
<span data-ttu-id="8d823-116">Идентификатор партнера по управлению — номер 6 цифр.</span><span class="sxs-lookup"><span data-stu-id="8d823-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d823-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d823-117">CommonParameters</span></span>
<span data-ttu-id="8d823-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d823-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d823-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d823-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d823-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d823-120">INPUTS</span></span>

### <span data-ttu-id="8d823-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="8d823-121">None</span></span>

## <span data-ttu-id="8d823-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d823-122">OUTPUTS</span></span>

### <span data-ttu-id="8d823-123">Microsoft. Azure. Commands. Resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8d823-123">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="8d823-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d823-124">NOTES</span></span>

## <span data-ttu-id="8d823-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d823-125">RELATED LINKS</span></span>

[<span data-ttu-id="8d823-126">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8d823-126">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="8d823-127">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8d823-127">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="8d823-128">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="8d823-128">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
