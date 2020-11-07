---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 7542e9621d90ffdb19bb8db679592dd17a216d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732779"
---
# <span data-ttu-id="50539-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="50539-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="50539-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="50539-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50539-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="50539-103">SYNTAX</span></span>

### <span data-ttu-id="50539-104">Получить все свойства (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="50539-104">Get all properties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50539-105">Идентификатор свойства Get</span><span class="sxs-lookup"><span data-stu-id="50539-105">Get by property ID</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50539-106">Поиск свойств с именем</span><span class="sxs-lookup"><span data-stu-id="50539-106">Find properties containing Name</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50539-107">Поиск свойств по тегам</span><span class="sxs-lookup"><span data-stu-id="50539-107">Find properties by Tag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50539-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50539-108">DESCRIPTION</span></span>

## <span data-ttu-id="50539-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="50539-109">EXAMPLES</span></span>

### <span data-ttu-id="50539-110">1:</span><span class="sxs-lookup"><span data-stu-id="50539-110">1:</span></span>
```
PS C:\> Get-AzureRmApiManagementProperty -Context $Context -Name $PropertyName
```

## <span data-ttu-id="50539-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="50539-111">PARAMETERS</span></span>

### <span data-ttu-id="50539-112">-Context</span><span class="sxs-lookup"><span data-stu-id="50539-112">-Context</span></span>
```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50539-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="50539-113">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: Find properties containing Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50539-114">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="50539-114">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: Get by property ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50539-115">-Тег</span><span class="sxs-lookup"><span data-stu-id="50539-115">-Tag</span></span>
<span data-ttu-id="50539-116">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="50539-116">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="50539-117">Например:</span><span class="sxs-lookup"><span data-stu-id="50539-117">For example:</span></span>

<span data-ttu-id="50539-118">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="50539-118">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.String
Parameter Sets: Find properties by Tag
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50539-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50539-119">-DefaultProfile</span></span>
<span data-ttu-id="50539-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50539-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50539-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50539-121">CommonParameters</span></span>
<span data-ttu-id="50539-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="50539-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50539-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50539-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50539-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="50539-124">INPUTS</span></span>

## <span data-ttu-id="50539-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="50539-125">OUTPUTS</span></span>

### <span data-ttu-id="50539-126">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Systems. ApiManagement. ServiceManagement. Models. PsApiManagementProperty]</span><span class="sxs-lookup"><span data-stu-id="50539-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty]</span></span>

### <span data-ttu-id="50539-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="50539-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="50539-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="50539-128">NOTES</span></span>

## <span data-ttu-id="50539-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50539-129">RELATED LINKS</span></span>

