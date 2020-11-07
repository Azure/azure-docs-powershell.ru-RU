---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: c636da952c02b4f2b4795cd1703c276a23a8221c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720172"
---
# <span data-ttu-id="400be-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="400be-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="400be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="400be-102">SYNOPSIS</span></span>
<span data-ttu-id="400be-103">Возвращает список или определенное описание службы управления API.</span><span class="sxs-lookup"><span data-stu-id="400be-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="400be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="400be-104">SYNTAX</span></span>

### <span data-ttu-id="400be-105">GetBySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="400be-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="400be-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="400be-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="400be-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="400be-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="400be-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="400be-108">DESCRIPTION</span></span>
<span data-ttu-id="400be-109">Командлет **Get-AzApiManagement** возвращает список всех служб управления API в разделе Подписка или указанную группу ресурсов или ОПРЕДЕЛЕННОЕ управление API.</span><span class="sxs-lookup"><span data-stu-id="400be-109">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="400be-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="400be-110">EXAMPLES</span></span>

### <span data-ttu-id="400be-111">Пример 1: получение всех служб управления API</span><span class="sxs-lookup"><span data-stu-id="400be-111">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="400be-112">Эта команда получает все службы управления API в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="400be-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="400be-113">Пример 2: получение всех служб управления API по определенному имени</span><span class="sxs-lookup"><span data-stu-id="400be-113">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="400be-114">Эта команда получает все службы управления API по имени.</span><span class="sxs-lookup"><span data-stu-id="400be-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="400be-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="400be-115">PARAMETERS</span></span>

### <span data-ttu-id="400be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="400be-116">-DefaultProfile</span></span>
<span data-ttu-id="400be-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="400be-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="400be-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="400be-118">-Name</span></span>
<span data-ttu-id="400be-119">Указывает имя службы управления API.</span><span class="sxs-lookup"><span data-stu-id="400be-119">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="400be-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="400be-120">-ResourceGroupName</span></span>
<span data-ttu-id="400be-121">Указывает имя группы ресурсов, в которой этот командлет получает службу управления API.</span><span class="sxs-lookup"><span data-stu-id="400be-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="400be-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="400be-122">CommonParameters</span></span>
<span data-ttu-id="400be-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="400be-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="400be-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="400be-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="400be-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="400be-125">INPUTS</span></span>

### <span data-ttu-id="400be-126">System. String</span><span class="sxs-lookup"><span data-stu-id="400be-126">System.String</span></span>

## <span data-ttu-id="400be-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="400be-127">OUTPUTS</span></span>

### <span data-ttu-id="400be-128">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="400be-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="400be-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="400be-129">NOTES</span></span>

## <span data-ttu-id="400be-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="400be-130">RELATED LINKS</span></span>

[<span data-ttu-id="400be-131">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="400be-131">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="400be-132">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="400be-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="400be-133">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="400be-133">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="400be-134">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="400be-134">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


