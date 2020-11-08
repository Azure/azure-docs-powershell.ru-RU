---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078019"
---
# <span data-ttu-id="bdfc8-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="bdfc8-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="bdfc8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bdfc8-102">SYNOPSIS</span></span>
<span data-ttu-id="bdfc8-103">Возвращает список или определенное именованное значение.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="bdfc8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bdfc8-104">SYNTAX</span></span>

### <span data-ttu-id="bdfc8-105">GetAllNamedValues (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bdfc8-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bdfc8-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="bdfc8-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdfc8-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="bdfc8-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdfc8-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="bdfc8-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdfc8-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdfc8-109">DESCRIPTION</span></span>
<span data-ttu-id="bdfc8-110">Командлет **Get-AzApiManagementNamedValue** возвращает список или определенное именованное значение.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="bdfc8-111">Значение не будет включено в результирующие данные, если именованное значение помечено как секретное.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="bdfc8-112">Чтобы получить секретное значение, используйте **Get-AzApiManagementNamedValueSecretValue**.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="bdfc8-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bdfc8-113">EXAMPLES</span></span>

### <span data-ttu-id="bdfc8-114">Пример 1: получение именованного значения по имени</span><span class="sxs-lookup"><span data-stu-id="bdfc8-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="bdfc8-115">Эта команда возвращает сведения о названии значения с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="bdfc8-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bdfc8-116">PARAMETERS</span></span>

### <span data-ttu-id="bdfc8-117">-Context</span><span class="sxs-lookup"><span data-stu-id="bdfc8-117">-Context</span></span>
<span data-ttu-id="bdfc8-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bdfc8-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdfc8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdfc8-120">-DefaultProfile</span></span>
<span data-ttu-id="bdfc8-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdfc8-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bdfc8-122">-Name</span></span>
<span data-ttu-id="bdfc8-123">Находит именованные значения с именами, содержащими строковое имя.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="bdfc8-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdfc8-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="bdfc8-125">-NamedValueId</span></span>
<span data-ttu-id="bdfc8-126">Идентификатор именованного значения.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-126">Identifier of the named value.</span></span>
<span data-ttu-id="bdfc8-127">Если задано значение, это попытается найти имя с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="bdfc8-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-128">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdfc8-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="bdfc8-129">-Tag</span></span>
<span data-ttu-id="bdfc8-130">Поиск именованных значений, связанных с тегом.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="bdfc8-131">Если задано значение, будут возвращены все свойства, связанные с тегом.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="bdfc8-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-132">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdfc8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdfc8-133">CommonParameters</span></span>
<span data-ttu-id="bdfc8-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bdfc8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdfc8-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdfc8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdfc8-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bdfc8-136">INPUTS</span></span>

### <span data-ttu-id="bdfc8-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bdfc8-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bdfc8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bdfc8-138">System.String</span></span>

## <span data-ttu-id="bdfc8-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdfc8-139">OUTPUTS</span></span>

### <span data-ttu-id="bdfc8-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="bdfc8-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="bdfc8-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="bdfc8-141">NOTES</span></span>

## <span data-ttu-id="bdfc8-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bdfc8-142">RELATED LINKS</span></span>
