---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393054
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
ms.openlocfilehash: 420353d7a8af1046456138918092ca56d5c6ed96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565385"
---
# <span data-ttu-id="01423-101">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="01423-101">Update-AzureRmManagementPartner</span></span>

## <span data-ttu-id="01423-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01423-102">SYNOPSIS</span></span>
<span data-ttu-id="01423-103">Обновляет идентификационный номер сети партнера Майкрософт (MPN) текущего пользователя или участника-службы, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="01423-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01423-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01423-104">SYNTAX</span></span>

```
Update-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01423-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01423-105">DESCRIPTION</span></span>
<span data-ttu-id="01423-106">Обновляет идентификационный номер сети партнера Майкрософт (MPN) текущего пользователя или участника-службы, прошедшего проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="01423-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="01423-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01423-107">EXAMPLES</span></span>

### <span data-ttu-id="01423-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="01423-108">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="01423-109">Обновление партнера по управлению на новый</span><span class="sxs-lookup"><span data-stu-id="01423-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="01423-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01423-110">PARAMETERS</span></span>

### <span data-ttu-id="01423-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01423-111">-DefaultProfile</span></span>
<span data-ttu-id="01423-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01423-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01423-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="01423-113">-PartnerId</span></span>
<span data-ttu-id="01423-114">Идентификатор партнера по управлению — номер 6 цифр.</span><span class="sxs-lookup"><span data-stu-id="01423-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="01423-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01423-115">-Confirm</span></span>
<span data-ttu-id="01423-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="01423-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01423-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01423-117">-WhatIf</span></span>
<span data-ttu-id="01423-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="01423-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01423-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="01423-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01423-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01423-120">CommonParameters</span></span>
<span data-ttu-id="01423-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01423-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01423-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01423-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01423-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01423-123">INPUTS</span></span>

### <span data-ttu-id="01423-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="01423-124">None</span></span>

## <span data-ttu-id="01423-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01423-125">OUTPUTS</span></span>

### <span data-ttu-id="01423-126">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="01423-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="01423-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="01423-127">NOTES</span></span>

## <span data-ttu-id="01423-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01423-128">RELATED LINKS</span></span>

[<span data-ttu-id="01423-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="01423-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="01423-130">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="01423-130">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="01423-131">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="01423-131">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)
