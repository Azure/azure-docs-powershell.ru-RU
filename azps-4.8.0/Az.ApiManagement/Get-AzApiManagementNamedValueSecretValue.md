---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079256"
---
# <span data-ttu-id="53ac5-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="53ac5-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="53ac5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="53ac5-102">SYNOPSIS</span></span>
<span data-ttu-id="53ac5-103">Возвращает секретное значение определенного именованного значения.</span><span class="sxs-lookup"><span data-stu-id="53ac5-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="53ac5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="53ac5-104">SYNTAX</span></span>

### <span data-ttu-id="53ac5-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="53ac5-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53ac5-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="53ac5-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53ac5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53ac5-107">DESCRIPTION</span></span>
<span data-ttu-id="53ac5-108">Возвращает секретное значение определенного именованного значения.</span><span class="sxs-lookup"><span data-stu-id="53ac5-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="53ac5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="53ac5-109">EXAMPLES</span></span>

### <span data-ttu-id="53ac5-110">Пример 1: получение именованного значения по имени</span><span class="sxs-lookup"><span data-stu-id="53ac5-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="53ac5-111">Эта команда возвращает сведения о названии значения с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="53ac5-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="53ac5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="53ac5-112">PARAMETERS</span></span>

### <span data-ttu-id="53ac5-113">-Context</span><span class="sxs-lookup"><span data-stu-id="53ac5-113">-Context</span></span>
<span data-ttu-id="53ac5-114">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="53ac5-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="53ac5-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="53ac5-115">This parameter is required.</span></span>

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

### <span data-ttu-id="53ac5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53ac5-116">-DefaultProfile</span></span>
<span data-ttu-id="53ac5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53ac5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53ac5-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="53ac5-118">-NamedValueId</span></span>
<span data-ttu-id="53ac5-119">Идентификатор именованного значения.</span><span class="sxs-lookup"><span data-stu-id="53ac5-119">Identifier of a the named value.</span></span>
<span data-ttu-id="53ac5-120">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="53ac5-120">This parameter is required.</span></span>

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

### <span data-ttu-id="53ac5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53ac5-121">CommonParameters</span></span>
<span data-ttu-id="53ac5-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="53ac5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53ac5-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53ac5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53ac5-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="53ac5-124">INPUTS</span></span>

### <span data-ttu-id="53ac5-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="53ac5-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="53ac5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="53ac5-126">System.String</span></span>

## <span data-ttu-id="53ac5-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="53ac5-127">OUTPUTS</span></span>

### <span data-ttu-id="53ac5-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="53ac5-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="53ac5-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="53ac5-129">NOTES</span></span>

## <span data-ttu-id="53ac5-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53ac5-130">RELATED LINKS</span></span>
