---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 41f7b921cb1977d7410c511be224b7e24623597b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315428"
---
# <span data-ttu-id="268d8-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="268d8-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="268d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="268d8-102">SYNOPSIS</span></span>
<span data-ttu-id="268d8-103">Возвращает список или определенное описание службы управления API.</span><span class="sxs-lookup"><span data-stu-id="268d8-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="268d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="268d8-104">SYNTAX</span></span>

### <span data-ttu-id="268d8-105">GetBySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="268d8-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268d8-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="268d8-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268d8-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="268d8-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="268d8-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="268d8-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="268d8-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="268d8-109">DESCRIPTION</span></span>
<span data-ttu-id="268d8-110">Командлет **Get-AzApiManagement** возвращает список всех служб управления API в разделе Подписка или указанную группу ресурсов или ОПРЕДЕЛЕННОЕ управление API.</span><span class="sxs-lookup"><span data-stu-id="268d8-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="268d8-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="268d8-111">EXAMPLES</span></span>

### <span data-ttu-id="268d8-112">Пример 1: получение всех служб управления API</span><span class="sxs-lookup"><span data-stu-id="268d8-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="268d8-113">Эта команда получает все службы управления API в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="268d8-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="268d8-114">Пример 2: получение всех служб управления API по определенному имени</span><span class="sxs-lookup"><span data-stu-id="268d8-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="268d8-115">Эта команда получает все службы управления API по имени.</span><span class="sxs-lookup"><span data-stu-id="268d8-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="268d8-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="268d8-116">PARAMETERS</span></span>

### <span data-ttu-id="268d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268d8-117">-DefaultProfile</span></span>
<span data-ttu-id="268d8-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="268d8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="268d8-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="268d8-119">-Name</span></span>
<span data-ttu-id="268d8-120">Указывает имя службы управления API.</span><span class="sxs-lookup"><span data-stu-id="268d8-120">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="268d8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="268d8-121">-ResourceGroupName</span></span>
<span data-ttu-id="268d8-122">Указывает имя группы ресурсов, в которой этот командлет получает службу управления API.</span><span class="sxs-lookup"><span data-stu-id="268d8-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="268d8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="268d8-123">-ResourceId</span></span>
<span data-ttu-id="268d8-124">ResourceId (ИД ресурса) службы управления API.</span><span class="sxs-lookup"><span data-stu-id="268d8-124">Arm ResourceId of the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268d8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268d8-125">CommonParameters</span></span>
<span data-ttu-id="268d8-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="268d8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268d8-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="268d8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268d8-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="268d8-128">INPUTS</span></span>

### <span data-ttu-id="268d8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="268d8-129">System.String</span></span>

## <span data-ttu-id="268d8-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="268d8-130">OUTPUTS</span></span>

### <span data-ttu-id="268d8-131">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="268d8-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="268d8-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="268d8-132">NOTES</span></span>

## <span data-ttu-id="268d8-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="268d8-133">RELATED LINKS</span></span>

[<span data-ttu-id="268d8-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="268d8-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="268d8-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="268d8-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="268d8-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="268d8-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="268d8-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="268d8-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)

