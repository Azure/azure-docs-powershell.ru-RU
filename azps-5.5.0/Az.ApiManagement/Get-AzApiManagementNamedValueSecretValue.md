---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239797"
---
# <span data-ttu-id="e5c86-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="e5c86-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="e5c86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5c86-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c86-103">Получает секретную величину определенного именоваемого значения.</span><span class="sxs-lookup"><span data-stu-id="e5c86-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="e5c86-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e5c86-104">SYNTAX</span></span>

### <span data-ttu-id="e5c86-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5c86-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c86-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="e5c86-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5c86-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5c86-107">DESCRIPTION</span></span>
<span data-ttu-id="e5c86-108">Получает секретную величину определенного именоваемого значения.</span><span class="sxs-lookup"><span data-stu-id="e5c86-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="e5c86-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e5c86-109">EXAMPLES</span></span>

### <span data-ttu-id="e5c86-110">Пример 1. Получить именуемую величину по имени</span><span class="sxs-lookup"><span data-stu-id="e5c86-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="e5c86-111">Эта команда получает сведения об именоваемом значении с именем.</span><span class="sxs-lookup"><span data-stu-id="e5c86-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="e5c86-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5c86-112">PARAMETERS</span></span>

### <span data-ttu-id="e5c86-113">-Контекст</span><span class="sxs-lookup"><span data-stu-id="e5c86-113">-Context</span></span>
<span data-ttu-id="e5c86-114">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e5c86-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e5c86-115">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="e5c86-115">This parameter is required.</span></span>

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

### <span data-ttu-id="e5c86-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c86-116">-DefaultProfile</span></span>
<span data-ttu-id="e5c86-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c86-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5c86-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="e5c86-118">-NamedValueId</span></span>
<span data-ttu-id="e5c86-119">Идентификатор именоваемого значения.</span><span class="sxs-lookup"><span data-stu-id="e5c86-119">Identifier of a the named value.</span></span>
<span data-ttu-id="e5c86-120">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="e5c86-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c86-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c86-121">CommonParameters</span></span>
<span data-ttu-id="e5c86-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5c86-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c86-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5c86-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c86-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5c86-124">INPUTS</span></span>

### <span data-ttu-id="e5c86-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e5c86-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e5c86-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e5c86-126">System.String</span></span>

## <span data-ttu-id="e5c86-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5c86-127">OUTPUTS</span></span>

### <span data-ttu-id="e5c86-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="e5c86-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="e5c86-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e5c86-129">NOTES</span></span>

## <span data-ttu-id="e5c86-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5c86-130">RELATED LINKS</span></span>
