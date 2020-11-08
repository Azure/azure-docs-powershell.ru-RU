---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079235"
---
# <span data-ttu-id="e018c-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="e018c-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="e018c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e018c-102">SYNOPSIS</span></span>
<span data-ttu-id="e018c-103">Создайте новый контракт о расположении ресурсов (используется в шлюзах).</span><span class="sxs-lookup"><span data-stu-id="e018c-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="e018c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e018c-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e018c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e018c-105">DESCRIPTION</span></span>
<span data-ttu-id="e018c-106">Командлет **New-AzApiManagementResourceLocationObject** создает новый контракт о расположении ресурсов (используется в шлюзах).</span><span class="sxs-lookup"><span data-stu-id="e018c-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="e018c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e018c-107">EXAMPLES</span></span>

### <span data-ttu-id="e018c-108">Пример 1: Создание контракта на расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="e018c-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="e018c-109">Эта команда создает расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="e018c-109">This command creates a resource location.</span></span>

## <span data-ttu-id="e018c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e018c-110">PARAMETERS</span></span>

### <span data-ttu-id="e018c-111">-Город</span><span class="sxs-lookup"><span data-stu-id="e018c-111">-City</span></span>
<span data-ttu-id="e018c-112">Город "место".</span><span class="sxs-lookup"><span data-stu-id="e018c-112">Location City.</span></span>
<span data-ttu-id="e018c-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e018c-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e018c-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="e018c-114">-CountryOrRegion</span></span>
<span data-ttu-id="e018c-115">Страна или регион местонахождения.</span><span class="sxs-lookup"><span data-stu-id="e018c-115">Location Country or Region.</span></span>
<span data-ttu-id="e018c-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e018c-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e018c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e018c-117">-DefaultProfile</span></span>
<span data-ttu-id="e018c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e018c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e018c-119">-Округ</span><span class="sxs-lookup"><span data-stu-id="e018c-119">-District</span></span>
<span data-ttu-id="e018c-120">Район места.</span><span class="sxs-lookup"><span data-stu-id="e018c-120">Location District.</span></span>
<span data-ttu-id="e018c-121">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e018c-121">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e018c-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e018c-122">-Name</span></span>
<span data-ttu-id="e018c-123">Название местоположения.</span><span class="sxs-lookup"><span data-stu-id="e018c-123">Location Name.</span></span>
<span data-ttu-id="e018c-124">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e018c-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e018c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e018c-125">CommonParameters</span></span>
<span data-ttu-id="e018c-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e018c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e018c-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e018c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e018c-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e018c-128">INPUTS</span></span>

### <span data-ttu-id="e018c-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="e018c-129">None</span></span>

## <span data-ttu-id="e018c-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e018c-130">OUTPUTS</span></span>

### <span data-ttu-id="e018c-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="e018c-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="e018c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="e018c-132">NOTES</span></span>

## <span data-ttu-id="e018c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e018c-133">RELATED LINKS</span></span>
