---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
ms.openlocfilehash: a1ca7766efc79d3d9db2d8feef94a2bb7aab9c36
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066392"
---
# <span data-ttu-id="31aa1-101">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="31aa1-101">Get-AzApiManagementProperty</span></span>

## <span data-ttu-id="31aa1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="31aa1-103">Возвращает список или определенное свойство (именованное значение).</span><span class="sxs-lookup"><span data-stu-id="31aa1-103">Gets a list or a particular Property (Named-Value).</span></span>

## <span data-ttu-id="31aa1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31aa1-104">SYNTAX</span></span>

### <span data-ttu-id="31aa1-105">GetAllProperties (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31aa1-105">GetAllProperties (Default)</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31aa1-106">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="31aa1-106">GetByPropertyId</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31aa1-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="31aa1-107">GetByName</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31aa1-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="31aa1-108">GetByTag</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31aa1-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31aa1-109">DESCRIPTION</span></span>
<span data-ttu-id="31aa1-110">Командлет **Get-AzApiManagementProperty** получает список или определенное свойство.</span><span class="sxs-lookup"><span data-stu-id="31aa1-110">The **Get-AzApiManagementProperty** cmdlet gets a list or a particular property.</span></span>

## <span data-ttu-id="31aa1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31aa1-111">EXAMPLES</span></span>

### <span data-ttu-id="31aa1-112">Пример 1: получение свойства по имени</span><span class="sxs-lookup"><span data-stu-id="31aa1-112">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="31aa1-113">Эта команда получает сведения о свойстве с заданным именем свойства.</span><span class="sxs-lookup"><span data-stu-id="31aa1-113">This command gets the property details given the property name.</span></span>

## <span data-ttu-id="31aa1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31aa1-114">PARAMETERS</span></span>

### <span data-ttu-id="31aa1-115">-Context</span><span class="sxs-lookup"><span data-stu-id="31aa1-115">-Context</span></span>
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

### <span data-ttu-id="31aa1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31aa1-116">-DefaultProfile</span></span>
<span data-ttu-id="31aa1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31aa1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31aa1-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31aa1-118">-Name</span></span>
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

### <span data-ttu-id="31aa1-119">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="31aa1-119">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByPropertyId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31aa1-120">-Тег</span><span class="sxs-lookup"><span data-stu-id="31aa1-120">-Tag</span></span>
<span data-ttu-id="31aa1-121">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="31aa1-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="31aa1-122">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="31aa1-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="31aa1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31aa1-123">CommonParameters</span></span>
<span data-ttu-id="31aa1-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31aa1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31aa1-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31aa1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31aa1-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31aa1-126">INPUTS</span></span>

### <span data-ttu-id="31aa1-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="31aa1-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="31aa1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="31aa1-128">System.String</span></span>

## <span data-ttu-id="31aa1-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31aa1-129">OUTPUTS</span></span>

### <span data-ttu-id="31aa1-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="31aa1-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="31aa1-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="31aa1-131">NOTES</span></span>

## <span data-ttu-id="31aa1-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31aa1-132">RELATED LINKS</span></span>
