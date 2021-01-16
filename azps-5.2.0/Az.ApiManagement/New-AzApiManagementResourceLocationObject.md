---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409543"
---
# <span data-ttu-id="3ff7b-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="3ff7b-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="3ff7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ff7b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff7b-103">Создать новый контракт с расположением ресурса (используется в шлюзах).</span><span class="sxs-lookup"><span data-stu-id="3ff7b-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="3ff7b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3ff7b-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ff7b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ff7b-105">DESCRIPTION</span></span>
<span data-ttu-id="3ff7b-106">Для создания нового контракта с расположением ресурса (используется в шлюзах) используется новый проект **AzApiManagementResourceLocationObject.**</span><span class="sxs-lookup"><span data-stu-id="3ff7b-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="3ff7b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3ff7b-107">EXAMPLES</span></span>

### <span data-ttu-id="3ff7b-108">Пример 1. Создание контракта с расположением ресурса</span><span class="sxs-lookup"><span data-stu-id="3ff7b-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="3ff7b-109">Эта команда создает расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="3ff7b-109">This command creates a resource location.</span></span>

## <span data-ttu-id="3ff7b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ff7b-110">PARAMETERS</span></span>

### <span data-ttu-id="3ff7b-111">-Город</span><span class="sxs-lookup"><span data-stu-id="3ff7b-111">-City</span></span>
<span data-ttu-id="3ff7b-112">"Город расположения".</span><span class="sxs-lookup"><span data-stu-id="3ff7b-112">Location City.</span></span>
<span data-ttu-id="3ff7b-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3ff7b-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="3ff7b-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="3ff7b-114">-CountryOrRegion</span></span>
<span data-ttu-id="3ff7b-115">Страна или регион расположения.</span><span class="sxs-lookup"><span data-stu-id="3ff7b-115">Location Country or Region.</span></span>
<span data-ttu-id="3ff7b-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3ff7b-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="3ff7b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff7b-117">-DefaultProfile</span></span>
<span data-ttu-id="3ff7b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ff7b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ff7b-119">-District</span><span class="sxs-lookup"><span data-stu-id="3ff7b-119">-District</span></span>
<span data-ttu-id="3ff7b-120">Область расположения.</span><span class="sxs-lookup"><span data-stu-id="3ff7b-120">Location District.</span></span>
<span data-ttu-id="3ff7b-121">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3ff7b-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="3ff7b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3ff7b-122">-Name</span></span>
<span data-ttu-id="3ff7b-123">Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="3ff7b-123">Location Name.</span></span>
<span data-ttu-id="3ff7b-124">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="3ff7b-124">This parameter is required.</span></span>

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

### <span data-ttu-id="3ff7b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff7b-125">CommonParameters</span></span>
<span data-ttu-id="3ff7b-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ff7b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff7b-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ff7b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff7b-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ff7b-128">INPUTS</span></span>

### <span data-ttu-id="3ff7b-129">Нет</span><span class="sxs-lookup"><span data-stu-id="3ff7b-129">None</span></span>

## <span data-ttu-id="3ff7b-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3ff7b-130">OUTPUTS</span></span>

### <span data-ttu-id="3ff7b-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="3ff7b-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="3ff7b-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3ff7b-132">NOTES</span></span>

## <span data-ttu-id="3ff7b-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ff7b-133">RELATED LINKS</span></span>