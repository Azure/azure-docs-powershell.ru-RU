---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: f14da4760f70c8e4ba95136b81a884f830f4f44a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242689"
---
# <span data-ttu-id="20be0-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="20be0-101">Get-AzLocation</span></span>

## <span data-ttu-id="20be0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20be0-102">SYNOPSIS</span></span>
<span data-ttu-id="20be0-103">Получает все расположения и поддерживаемые поставщики ресурсов для каждого местоположения.</span><span class="sxs-lookup"><span data-stu-id="20be0-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="20be0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20be0-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20be0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20be0-105">DESCRIPTION</span></span>
<span data-ttu-id="20be0-106">Командлет **Get-AzLocation** получает все расположения и поддерживаемые поставщики ресурсов для каждого местоположения.</span><span class="sxs-lookup"><span data-stu-id="20be0-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="20be0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20be0-107">EXAMPLES</span></span>

### <span data-ttu-id="20be0-108">Пример 1: получение всех местоположений и поддерживаемых поставщиков ресурсов</span><span class="sxs-lookup"><span data-stu-id="20be0-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="20be0-109">Эта команда получает все расположения и поддерживаемые поставщики ресурсов для каждого местоположения.</span><span class="sxs-lookup"><span data-stu-id="20be0-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="20be0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20be0-110">PARAMETERS</span></span>

### <span data-ttu-id="20be0-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="20be0-111">-ApiVersion</span></span>
<span data-ttu-id="20be0-112">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="20be0-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="20be0-113">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20be0-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="20be0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20be0-114">-DefaultProfile</span></span>
<span data-ttu-id="20be0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="20be0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20be0-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="20be0-116">-Pre</span></span>
<span data-ttu-id="20be0-117">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="20be0-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="20be0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20be0-118">CommonParameters</span></span>
<span data-ttu-id="20be0-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20be0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20be0-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20be0-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20be0-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20be0-121">INPUTS</span></span>

### <span data-ttu-id="20be0-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="20be0-122">None</span></span>

## <span data-ttu-id="20be0-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20be0-123">OUTPUTS</span></span>

### <span data-ttu-id="20be0-124">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="20be0-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="20be0-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="20be0-125">NOTES</span></span>

## <span data-ttu-id="20be0-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20be0-126">RELATED LINKS</span></span>