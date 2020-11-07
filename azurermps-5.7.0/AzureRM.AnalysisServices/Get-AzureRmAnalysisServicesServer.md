---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/get-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: f67c22b483b561af8ffcf2ede9bc1e489379c0d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733293"
---
# <span data-ttu-id="d62fe-101">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d62fe-101">Get-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="d62fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d62fe-102">SYNOPSIS</span></span>
<span data-ttu-id="d62fe-103">Получает сведения о сервере служб Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="d62fe-103">Gets the details of an Analysis Services server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d62fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d62fe-104">SYNTAX</span></span>

```
Get-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d62fe-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d62fe-105">DESCRIPTION</span></span>
<span data-ttu-id="d62fe-106">Командлет Get-AzureRmAnalysisServicesServer получает сведения о сервере служб Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="d62fe-106">The Get-AzureRmAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="d62fe-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d62fe-107">EXAMPLES</span></span>

### <span data-ttu-id="d62fe-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d62fe-108">Example 1</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="d62fe-109">Эта команда получает все серверы служб аналитики Azure в группе ресурсов с именем ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="d62fe-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="d62fe-110">Пример 2: получение сервера</span><span class="sxs-lookup"><span data-stu-id="d62fe-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="d62fe-111">Эта команда получает сервер служб аналитики Azure с именем TestServer в группе ресурсов с именем ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="d62fe-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="d62fe-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d62fe-112">PARAMETERS</span></span>

### <span data-ttu-id="d62fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d62fe-113">-DefaultProfile</span></span>
<span data-ttu-id="d62fe-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d62fe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d62fe-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d62fe-115">-Name</span></span>
<span data-ttu-id="d62fe-116">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="d62fe-116">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d62fe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d62fe-117">-ResourceGroupName</span></span>
<span data-ttu-id="d62fe-118">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="d62fe-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d62fe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d62fe-119">CommonParameters</span></span>
<span data-ttu-id="d62fe-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d62fe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d62fe-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d62fe-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d62fe-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d62fe-122">INPUTS</span></span>

### <span data-ttu-id="d62fe-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="d62fe-123">None</span></span>
<span data-ttu-id="d62fe-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d62fe-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d62fe-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d62fe-125">OUTPUTS</span></span>

### <span data-ttu-id="d62fe-126">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d62fe-126">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="d62fe-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="d62fe-127">NOTES</span></span>
<span data-ttu-id="d62fe-128">Alias (псевдоним): Get-AzureAs</span><span class="sxs-lookup"><span data-stu-id="d62fe-128">Alias: Get-AzureAs</span></span>

## <span data-ttu-id="d62fe-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d62fe-129">RELATED LINKS</span></span>

[<span data-ttu-id="d62fe-130">New-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="d62fe-130">New-AzureRmAnalysisServicesServer </span></span>](./New-AzureRmAnalysisServicesServer .md)

[<span data-ttu-id="d62fe-131">Remove-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="d62fe-131">Remove-AzureRmAnalysisServicesServer </span></span>](./Remove-AzureRmAnalysisServicesServer .md)
