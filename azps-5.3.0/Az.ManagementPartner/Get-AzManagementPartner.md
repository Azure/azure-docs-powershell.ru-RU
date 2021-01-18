---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: 1031c9c8828969d16097953aa7440e2c8c0a8c1b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508213"
---
# <span data-ttu-id="0570d-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0570d-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="0570d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0570d-102">SYNOPSIS</span></span>
<span data-ttu-id="0570d-103">Получает идентификацию текущего пользователя, который является авториентом или главой службы, в microsoft Partner Network(MPN).</span><span class="sxs-lookup"><span data-stu-id="0570d-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="0570d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0570d-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0570d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0570d-105">DESCRIPTION</span></span>
<span data-ttu-id="0570d-106">Получает идентификацию текущего пользователя, который является авториентом или главой службы, в microsoft Partner Network(MPN).</span><span class="sxs-lookup"><span data-stu-id="0570d-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="0570d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0570d-107">EXAMPLES</span></span>

### <span data-ttu-id="0570d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0570d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="0570d-109">Получить текущий ИД партнера по управлению</span><span class="sxs-lookup"><span data-stu-id="0570d-109">Get the current management partner id</span></span>

### <span data-ttu-id="0570d-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0570d-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="0570d-111">Получите текущий ИД партнера по управлению с помощью его ид. Если он не совпадает, он не будет работать</span><span class="sxs-lookup"><span data-stu-id="0570d-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="0570d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0570d-112">PARAMETERS</span></span>

### <span data-ttu-id="0570d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0570d-113">-DefaultProfile</span></span>
<span data-ttu-id="0570d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0570d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0570d-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="0570d-115">-PartnerId</span></span>
<span data-ttu-id="0570d-116">Номер партнера по управлению — 6 цифр.</span><span class="sxs-lookup"><span data-stu-id="0570d-116">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="0570d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0570d-117">CommonParameters</span></span>
<span data-ttu-id="0570d-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0570d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0570d-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0570d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0570d-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0570d-120">INPUTS</span></span>

### <span data-ttu-id="0570d-121">Нет</span><span class="sxs-lookup"><span data-stu-id="0570d-121">None</span></span>

## <span data-ttu-id="0570d-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0570d-122">OUTPUTS</span></span>

### <span data-ttu-id="0570d-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0570d-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="0570d-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0570d-124">NOTES</span></span>

## <span data-ttu-id="0570d-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0570d-125">RELATED LINKS</span></span>

[<span data-ttu-id="0570d-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0570d-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="0570d-127">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0570d-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="0570d-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0570d-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)