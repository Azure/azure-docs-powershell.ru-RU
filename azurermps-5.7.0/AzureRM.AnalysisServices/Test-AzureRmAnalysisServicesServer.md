---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/test-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 9dd8a86d1e98268708d7b0a12448df109ee083f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569111"
---
# <span data-ttu-id="f1c53-101">Test-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f1c53-101">Test-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="f1c53-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1c53-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c53-103">Проверка существования экземпляра сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f1c53-103">Tests the existence of an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1c53-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1c53-104">SYNTAX</span></span>

```
Test-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1c53-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1c53-105">DESCRIPTION</span></span>
<span data-ttu-id="f1c53-106">Командлет Test-AzureRmAnalysisServicesServer проверяет наличие экземпляра сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f1c53-106">The Test-AzureRmAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="f1c53-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1c53-107">EXAMPLES</span></span>

### <span data-ttu-id="f1c53-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f1c53-108">Example 1</span></span>
```
PS C:\> Test-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="f1c53-109">Эта команда пройдет проверку на наличие сервера с именем TestServer в группе resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="f1c53-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="f1c53-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1c53-110">PARAMETERS</span></span>

### <span data-ttu-id="f1c53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c53-111">-DefaultProfile</span></span>
<span data-ttu-id="f1c53-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1c53-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1c53-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f1c53-113">-Name</span></span>
<span data-ttu-id="f1c53-114">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f1c53-114">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c53-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1c53-115">-ResourceGroupName</span></span>
<span data-ttu-id="f1c53-116">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="f1c53-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="f1c53-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c53-117">CommonParameters</span></span>
<span data-ttu-id="f1c53-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1c53-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c53-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1c53-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c53-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1c53-120">INPUTS</span></span>

### <span data-ttu-id="f1c53-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="f1c53-121">None</span></span>
<span data-ttu-id="f1c53-122">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f1c53-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f1c53-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1c53-123">OUTPUTS</span></span>

### <span data-ttu-id="f1c53-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f1c53-124">System.Boolean</span></span>

## <span data-ttu-id="f1c53-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1c53-125">NOTES</span></span>
<span data-ttu-id="f1c53-126">Alias (псевдоним): Test-AzureAs</span><span class="sxs-lookup"><span data-stu-id="f1c53-126">Alias: Test-AzureAs</span></span>

## <span data-ttu-id="f1c53-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1c53-127">RELATED LINKS</span></span>

[<span data-ttu-id="f1c53-128">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f1c53-128">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="f1c53-129">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f1c53-129">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
