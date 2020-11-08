---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: f14da4760f70c8e4ba95136b81a884f830f4f44a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066793"
---
# <span data-ttu-id="7d033-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="7d033-101">Get-AzLocation</span></span>

## <span data-ttu-id="7d033-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d033-102">SYNOPSIS</span></span>
<span data-ttu-id="7d033-103">Получает все расположения и поддерживаемые поставщики ресурсов для каждого местоположения.</span><span class="sxs-lookup"><span data-stu-id="7d033-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="7d033-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d033-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d033-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d033-105">DESCRIPTION</span></span>
<span data-ttu-id="7d033-106">Командлет **Get-AzLocation** получает все расположения и поддерживаемые поставщики ресурсов для каждого местоположения.</span><span class="sxs-lookup"><span data-stu-id="7d033-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="7d033-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d033-107">EXAMPLES</span></span>

### <span data-ttu-id="7d033-108">Пример 1: получение всех местоположений и поддерживаемых поставщиков ресурсов</span><span class="sxs-lookup"><span data-stu-id="7d033-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="7d033-109">Эта команда получает все расположения и поддерживаемые поставщики ресурсов для каждого местоположения.</span><span class="sxs-lookup"><span data-stu-id="7d033-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="7d033-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d033-110">PARAMETERS</span></span>

### <span data-ttu-id="7d033-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7d033-111">-ApiVersion</span></span>
<span data-ttu-id="7d033-112">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d033-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="7d033-113">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7d033-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="7d033-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d033-114">-DefaultProfile</span></span>
<span data-ttu-id="7d033-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7d033-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d033-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="7d033-116">-Pre</span></span>
<span data-ttu-id="7d033-117">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="7d033-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d033-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d033-118">CommonParameters</span></span>
<span data-ttu-id="7d033-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d033-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d033-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d033-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d033-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d033-121">INPUTS</span></span>

### <span data-ttu-id="7d033-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="7d033-122">None</span></span>

## <span data-ttu-id="7d033-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d033-123">OUTPUTS</span></span>

### <span data-ttu-id="7d033-124">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="7d033-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="7d033-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d033-125">NOTES</span></span>

## <span data-ttu-id="7d033-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d033-126">RELATED LINKS</span></span>
