---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsamplingsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
ms.openlocfilehash: 12f0aa4d198a93d1e392aa61294de6e5815196b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728025"
---
# <span data-ttu-id="e6610-101">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="e6610-101">New-AzApiManagementSamplingSetting</span></span>

## <span data-ttu-id="e6610-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6610-102">SYNOPSIS</span></span>
<span data-ttu-id="e6610-103">Создание нового параметра выборки для диагностики</span><span class="sxs-lookup"><span data-stu-id="e6610-103">Create a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="e6610-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6610-104">SYNTAX</span></span>

```
New-AzApiManagementSamplingSetting [-SamplingType <String>] [-SamplingPercentage <Double>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6610-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6610-105">DESCRIPTION</span></span>
<span data-ttu-id="e6610-106">Командлет **New-AzApiManagementSamplingSetting** создает новый параметр выборки для диагностики.</span><span class="sxs-lookup"><span data-stu-id="e6610-106">The cmdlet **New-AzApiManagementSamplingSetting** creates a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="e6610-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6610-107">EXAMPLES</span></span>

### <span data-ttu-id="e6610-108">Пример 1: создание основной настройки выборки</span><span class="sxs-lookup"><span data-stu-id="e6610-108">Example 1 : Create a basic Sampling setting</span></span>
```powershell
PS C:\> New-AzApiManagementSamplingSetting -SamplingType fixed -Percentage 100

SamplingType Percentage
------------ ----------
fixed               100
```

<span data-ttu-id="e6610-109">Создание параметра выборки `Fixed` типа с ведением журнала для 100% запросов и ответов</span><span class="sxs-lookup"><span data-stu-id="e6610-109">Creates a sampling setting of `Fixed` type with logging for 100% of the requests / responses</span></span>

## <span data-ttu-id="e6610-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6610-110">PARAMETERS</span></span>

### <span data-ttu-id="e6610-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6610-111">-DefaultProfile</span></span>
<span data-ttu-id="e6610-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6610-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6610-113">-SamplingPercentage</span><span class="sxs-lookup"><span data-stu-id="e6610-113">-SamplingPercentage</span></span>
<span data-ttu-id="e6610-114">Частота дискретизации для фиксированной частоты дискретизации.</span><span class="sxs-lookup"><span data-stu-id="e6610-114">Rate of Sampling for Fixed Rate Sampling.</span></span> <span data-ttu-id="e6610-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e6610-115">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6610-116">-SamplingType</span><span class="sxs-lookup"><span data-stu-id="e6610-116">-SamplingType</span></span>
<span data-ttu-id="e6610-117">Тип выборки.</span><span class="sxs-lookup"><span data-stu-id="e6610-117">The Type of Sampling.</span></span>
<span data-ttu-id="e6610-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e6610-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6610-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6610-119">CommonParameters</span></span>
<span data-ttu-id="e6610-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6610-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6610-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6610-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6610-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6610-122">INPUTS</span></span>

### <span data-ttu-id="e6610-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="e6610-123">None</span></span>

## <span data-ttu-id="e6610-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6610-124">OUTPUTS</span></span>

### <span data-ttu-id="e6610-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="e6610-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

## <span data-ttu-id="e6610-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6610-126">NOTES</span></span>

## <span data-ttu-id="e6610-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6610-127">RELATED LINKS</span></span>

[<span data-ttu-id="e6610-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e6610-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="e6610-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e6610-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="e6610-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e6610-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="e6610-131">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="e6610-131">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)
