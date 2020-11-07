---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermlocation
schema: 2.0.0
ms.openlocfilehash: c5d9d2131ff144f04794d2cf283aaf51ed1450e9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913998"
---
# <span data-ttu-id="2bb33-101">Get-AzureRmLocation</span><span class="sxs-lookup"><span data-stu-id="2bb33-101">Get-AzureRmLocation</span></span>

## <span data-ttu-id="2bb33-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2bb33-102">SYNOPSIS</span></span>
<span data-ttu-id="2bb33-103">Получает все расположения и поддерживаемые поставщики ресурсов для каждого местоположения.</span><span class="sxs-lookup"><span data-stu-id="2bb33-103">Gets all locations and the supported resource providers for each location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bb33-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2bb33-104">SYNTAX</span></span>

```
Get-AzureRmLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2bb33-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bb33-105">DESCRIPTION</span></span>
<span data-ttu-id="2bb33-106">Командлет **Get-AzureRmLocation** получает все расположения и поддерживаемые поставщики ресурсов для каждого местоположения.</span><span class="sxs-lookup"><span data-stu-id="2bb33-106">The **Get-AzureRmLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="2bb33-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2bb33-107">EXAMPLES</span></span>

### <span data-ttu-id="2bb33-108">Пример 1: получение всех местоположений и поддерживаемых поставщиков ресурсов</span><span class="sxs-lookup"><span data-stu-id="2bb33-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzureRmLocation
```

<span data-ttu-id="2bb33-109">Эта команда получает все расположения и поддерживаемые поставщики ресурсов для каждого местоположения.</span><span class="sxs-lookup"><span data-stu-id="2bb33-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="2bb33-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2bb33-110">PARAMETERS</span></span>

### <span data-ttu-id="2bb33-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2bb33-111">-ApiVersion</span></span>
<span data-ttu-id="2bb33-112">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2bb33-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="2bb33-113">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2bb33-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="2bb33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bb33-114">-DefaultProfile</span></span>
<span data-ttu-id="2bb33-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2bb33-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2bb33-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="2bb33-116">-Pre</span></span>
<span data-ttu-id="2bb33-117">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="2bb33-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2bb33-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bb33-118">CommonParameters</span></span>
<span data-ttu-id="2bb33-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2bb33-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bb33-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bb33-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bb33-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2bb33-121">INPUTS</span></span>

## <span data-ttu-id="2bb33-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bb33-122">OUTPUTS</span></span>

## <span data-ttu-id="2bb33-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="2bb33-123">NOTES</span></span>

## <span data-ttu-id="2bb33-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2bb33-124">RELATED LINKS</span></span>
