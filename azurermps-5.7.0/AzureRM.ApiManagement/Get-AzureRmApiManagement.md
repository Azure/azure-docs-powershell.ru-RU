---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: 50a548716019f3b5e80cde4b89ae666f5b6199ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734498"
---
# <span data-ttu-id="d6f0a-101">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="d6f0a-101">Get-AzureRmApiManagement</span></span>

## <span data-ttu-id="d6f0a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f0a-103">Возвращает список или определенное описание службы управления API.</span><span class="sxs-lookup"><span data-stu-id="d6f0a-103">Gets a list or a particular API Management Service description.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6f0a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6f0a-104">SYNTAX</span></span>

### <span data-ttu-id="d6f0a-105">GetBySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d6f0a-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6f0a-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d6f0a-106">GetByResourceGroup</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6f0a-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="d6f0a-107">GetByResource</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6f0a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6f0a-108">DESCRIPTION</span></span>
<span data-ttu-id="d6f0a-109">Командлет **Get-AzureRmApiManagement** возвращает список всех служб управления API в разделе Подписка или указанную группу ресурсов или ОПРЕДЕЛЕННОЕ управление API.</span><span class="sxs-lookup"><span data-stu-id="d6f0a-109">The **Get-AzureRmApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="d6f0a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6f0a-110">EXAMPLES</span></span>

### <span data-ttu-id="d6f0a-111">Пример 1: получение всех служб управления API</span><span class="sxs-lookup"><span data-stu-id="d6f0a-111">Example 1: Get all API Management services</span></span>
```
PS C:\>Get-AzureRmApiManagement
```

<span data-ttu-id="d6f0a-112">Эта команда получает все службы управления API в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="d6f0a-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="d6f0a-113">Пример 2: получение всех служб управления API по определенному имени</span><span class="sxs-lookup"><span data-stu-id="d6f0a-113">Example 2: Get all API Management services by a specific name</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="d6f0a-114">Эта команда получает все службы управления API по имени.</span><span class="sxs-lookup"><span data-stu-id="d6f0a-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="d6f0a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6f0a-115">PARAMETERS</span></span>

### <span data-ttu-id="d6f0a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f0a-116">-DefaultProfile</span></span>
<span data-ttu-id="d6f0a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6f0a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="d6f0a-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d6f0a-118">-Name</span></span>
<span data-ttu-id="d6f0a-119">Указывает имя службы управления API.</span><span class="sxs-lookup"><span data-stu-id="d6f0a-119">Specifies the name of API Management service.</span></span>

```yaml
Type: String
Parameter Sets: GetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f0a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f0a-120">-ResourceGroupName</span></span>
<span data-ttu-id="d6f0a-121">Указывает имя группы ресурсов, в которой этот командлет получает службу управления API.</span><span class="sxs-lookup"><span data-stu-id="d6f0a-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f0a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f0a-122">CommonParameters</span></span>
<span data-ttu-id="d6f0a-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6f0a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f0a-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f0a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f0a-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6f0a-125">INPUTS</span></span>

### <span data-ttu-id="d6f0a-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="d6f0a-126">None</span></span>
<span data-ttu-id="d6f0a-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d6f0a-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d6f0a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6f0a-128">OUTPUTS</span></span>

### <span data-ttu-id="d6f0a-129">System. Collections. Generic. List ' 1 [Microsoft. Azure. PsApiManagement]</span><span class="sxs-lookup"><span data-stu-id="d6f0a-129">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement]</span></span>

## <span data-ttu-id="d6f0a-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6f0a-130">NOTES</span></span>

## <span data-ttu-id="d6f0a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6f0a-131">RELATED LINKS</span></span>

[<span data-ttu-id="d6f0a-132">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="d6f0a-132">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="d6f0a-133">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="d6f0a-133">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="d6f0a-134">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="d6f0a-134">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="d6f0a-135">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="d6f0a-135">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


