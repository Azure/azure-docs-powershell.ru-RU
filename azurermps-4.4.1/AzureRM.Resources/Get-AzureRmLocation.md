---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmLocation.md
ms.openlocfilehash: 62acee0398c9530a54e02c2347bf384498b07196
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568684"
---
# <span data-ttu-id="26ff9-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="26ff9-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="26ff9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="26ff9-103">Получает все расположения и поддерживаемые поставщики ресурсов для каждого местоположения.</span><span class="sxs-lookup"><span data-stu-id="26ff9-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26ff9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26ff9-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="26ff9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26ff9-105">DESCRIPTION</span></span>
<span data-ttu-id="26ff9-106">Командлет **Get-AzureRmLocation** получает все расположения и поддерживаемые поставщики ресурсов для каждого местоположения.</span><span class="sxs-lookup"><span data-stu-id="26ff9-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="26ff9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26ff9-107">EXAMPLES</span></span>

### <span data-ttu-id="26ff9-108">Пример 1: получение всех местоположений и поддерживаемых поставщиков ресурсов</span><span class="sxs-lookup"><span data-stu-id="26ff9-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="26ff9-109">Эта команда получает все расположения и поддерживаемые поставщики ресурсов для каждого местоположения.</span><span class="sxs-lookup"><span data-stu-id="26ff9-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="26ff9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26ff9-110">PARAMETERS</span></span>

### <span data-ttu-id="26ff9-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="26ff9-111">-ApiVersion</span></span>
<span data-ttu-id="26ff9-112">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26ff9-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="26ff9-113">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="26ff9-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="26ff9-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="26ff9-114">-Pre</span></span>
<span data-ttu-id="26ff9-115">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="26ff9-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="26ff9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26ff9-116">-DefaultProfile</span></span>
<span data-ttu-id="26ff9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26ff9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26ff9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26ff9-118">CommonParameters</span></span>
<span data-ttu-id="26ff9-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26ff9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26ff9-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26ff9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26ff9-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26ff9-121">INPUTS</span></span>

## <span data-ttu-id="26ff9-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26ff9-122">OUTPUTS</span></span>

### <span data-ttu-id="26ff9-123">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceProviderLocation]</span><span class="sxs-lookup"><span data-stu-id="26ff9-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation]</span></span>

## <span data-ttu-id="26ff9-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="26ff9-124">NOTES</span></span>

## <span data-ttu-id="26ff9-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26ff9-125">RELATED LINKS</span></span>

