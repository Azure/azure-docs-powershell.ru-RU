---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317402"
---
# <span data-ttu-id="62428-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="62428-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="62428-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62428-102">SYNOPSIS</span></span>
<span data-ttu-id="62428-103">Возвращает секретное значение определенного именованного значения.</span><span class="sxs-lookup"><span data-stu-id="62428-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="62428-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62428-104">SYNTAX</span></span>

### <span data-ttu-id="62428-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62428-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62428-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="62428-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62428-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62428-107">DESCRIPTION</span></span>
<span data-ttu-id="62428-108">Возвращает секретное значение определенного именованного значения.</span><span class="sxs-lookup"><span data-stu-id="62428-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="62428-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62428-109">EXAMPLES</span></span>

### <span data-ttu-id="62428-110">Пример 1: получение именованного значения по имени</span><span class="sxs-lookup"><span data-stu-id="62428-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="62428-111">Эта команда возвращает сведения о названии значения с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="62428-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="62428-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62428-112">PARAMETERS</span></span>

### <span data-ttu-id="62428-113">-Context</span><span class="sxs-lookup"><span data-stu-id="62428-113">-Context</span></span>
<span data-ttu-id="62428-114">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="62428-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="62428-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="62428-115">This parameter is required.</span></span>

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

### <span data-ttu-id="62428-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62428-116">-DefaultProfile</span></span>
<span data-ttu-id="62428-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62428-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62428-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="62428-118">-NamedValueId</span></span>
<span data-ttu-id="62428-119">Идентификатор именованного значения.</span><span class="sxs-lookup"><span data-stu-id="62428-119">Identifier of a the named value.</span></span>
<span data-ttu-id="62428-120">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="62428-120">This parameter is required.</span></span>

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

### <span data-ttu-id="62428-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62428-121">CommonParameters</span></span>
<span data-ttu-id="62428-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62428-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62428-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62428-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62428-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62428-124">INPUTS</span></span>

### <span data-ttu-id="62428-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="62428-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="62428-126">System. String</span><span class="sxs-lookup"><span data-stu-id="62428-126">System.String</span></span>

## <span data-ttu-id="62428-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62428-127">OUTPUTS</span></span>

### <span data-ttu-id="62428-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="62428-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="62428-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="62428-129">NOTES</span></span>

## <span data-ttu-id="62428-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62428-130">RELATED LINKS</span></span>
