---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProperty.md
ms.openlocfilehash: ad6e2aebcc5a4edcf5acd3255385b0e78f317627
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720140"
---
# <span data-ttu-id="297d0-101">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="297d0-101">Get-AzApiManagementProperty</span></span>

## <span data-ttu-id="297d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="297d0-102">SYNOPSIS</span></span>
<span data-ttu-id="297d0-103">Возвращает список или определенное свойство (именованное значение).</span><span class="sxs-lookup"><span data-stu-id="297d0-103">Gets a list or a particular Property (Named-Value).</span></span>

## <span data-ttu-id="297d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="297d0-104">SYNTAX</span></span>

### <span data-ttu-id="297d0-105">GetAllProperties (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="297d0-105">GetAllProperties (Default)</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="297d0-106">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="297d0-106">GetByPropertyId</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="297d0-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="297d0-107">GetByName</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="297d0-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="297d0-108">GetByTag</span></span>
```
Get-AzApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="297d0-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="297d0-109">DESCRIPTION</span></span>
<span data-ttu-id="297d0-110">Командлет **Get-AzApiManagementProperty** получает список или определенное свойство.</span><span class="sxs-lookup"><span data-stu-id="297d0-110">The **Get-AzApiManagementProperty** cmdlet gets a list or a particular property.</span></span>

## <span data-ttu-id="297d0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="297d0-111">EXAMPLES</span></span>

### <span data-ttu-id="297d0-112">Пример 1: получение свойства по имени</span><span class="sxs-lookup"><span data-stu-id="297d0-112">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="297d0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="297d0-113">PARAMETERS</span></span>

### <span data-ttu-id="297d0-114">-Context</span><span class="sxs-lookup"><span data-stu-id="297d0-114">-Context</span></span>
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

### <span data-ttu-id="297d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="297d0-115">-DefaultProfile</span></span>
<span data-ttu-id="297d0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="297d0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="297d0-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="297d0-117">-Name</span></span>
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

### <span data-ttu-id="297d0-118">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="297d0-118">-PropertyId</span></span>
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

### <span data-ttu-id="297d0-119">-Тег</span><span class="sxs-lookup"><span data-stu-id="297d0-119">-Tag</span></span>
<span data-ttu-id="297d0-120">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="297d0-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="297d0-121">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="297d0-121">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="297d0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="297d0-122">CommonParameters</span></span>
<span data-ttu-id="297d0-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="297d0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="297d0-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="297d0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="297d0-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="297d0-125">INPUTS</span></span>

### <span data-ttu-id="297d0-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="297d0-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="297d0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="297d0-127">System.String</span></span>

## <span data-ttu-id="297d0-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="297d0-128">OUTPUTS</span></span>

### <span data-ttu-id="297d0-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="297d0-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="297d0-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="297d0-130">NOTES</span></span>

## <span data-ttu-id="297d0-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="297d0-131">RELATED LINKS</span></span>
