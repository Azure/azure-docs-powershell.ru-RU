---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 47167e0729ab3476c74124e16d6ae95901f57ad2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563792"
---
# <span data-ttu-id="c64b7-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="c64b7-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="c64b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c64b7-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c64b7-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c64b7-103">SYNTAX</span></span>

### <span data-ttu-id="c64b7-104">GetAllProperties (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c64b7-104">GetAllProperties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c64b7-105">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="c64b7-105">GetByPropertyId</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c64b7-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="c64b7-106">GetByName</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c64b7-107">GetByTag</span><span class="sxs-lookup"><span data-stu-id="c64b7-107">GetByTag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c64b7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c64b7-108">DESCRIPTION</span></span>

## <span data-ttu-id="c64b7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c64b7-109">EXAMPLES</span></span>

### <span data-ttu-id="c64b7-110">Пример 1: получение свойства по имени</span><span class="sxs-lookup"><span data-stu-id="c64b7-110">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="c64b7-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c64b7-111">PARAMETERS</span></span>

### <span data-ttu-id="c64b7-112">-Context</span><span class="sxs-lookup"><span data-stu-id="c64b7-112">-Context</span></span>
```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c64b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c64b7-113">-DefaultProfile</span></span>
<span data-ttu-id="c64b7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c64b7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="c64b7-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c64b7-115">-Name</span></span>
```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c64b7-116">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="c64b7-116">-PropertyId</span></span>
```yaml
Type: String
Parameter Sets: GetByPropertyId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c64b7-117">-Тег</span><span class="sxs-lookup"><span data-stu-id="c64b7-117">-Tag</span></span>
<span data-ttu-id="c64b7-118">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="c64b7-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c64b7-119">Например:</span><span class="sxs-lookup"><span data-stu-id="c64b7-119">For example:</span></span>

<span data-ttu-id="c64b7-120">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="c64b7-120">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: String
Parameter Sets: GetByTag
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c64b7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c64b7-121">CommonParameters</span></span>
<span data-ttu-id="c64b7-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c64b7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c64b7-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c64b7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c64b7-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c64b7-124">INPUTS</span></span>

### <span data-ttu-id="c64b7-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="c64b7-125">None</span></span>
<span data-ttu-id="c64b7-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c64b7-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c64b7-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c64b7-127">OUTPUTS</span></span>

### <span data-ttu-id="c64b7-128">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Systems. ApiManagement. ServiceManagement. Models. PsApiManagementProperty]</span><span class="sxs-lookup"><span data-stu-id="c64b7-128">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty]</span></span>

### <span data-ttu-id="c64b7-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="c64b7-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="c64b7-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="c64b7-130">NOTES</span></span>

## <span data-ttu-id="c64b7-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c64b7-131">RELATED LINKS</span></span>

