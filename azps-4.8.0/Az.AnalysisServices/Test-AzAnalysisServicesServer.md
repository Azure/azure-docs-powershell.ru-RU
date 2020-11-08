---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 86a82d5c82cdb775e7b07c6189244e494d14c4a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079267"
---
# <span data-ttu-id="33b65-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="33b65-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="33b65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="33b65-102">SYNOPSIS</span></span>
<span data-ttu-id="33b65-103">Проверка существования экземпляра сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="33b65-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="33b65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="33b65-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33b65-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33b65-105">DESCRIPTION</span></span>
<span data-ttu-id="33b65-106">Командлет Test-AzAnalysisServicesServer проверяет наличие экземпляра сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="33b65-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="33b65-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="33b65-107">EXAMPLES</span></span>

### <span data-ttu-id="33b65-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="33b65-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="33b65-109">Эта команда пройдет проверку на наличие сервера с именем TestServer в группе resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="33b65-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="33b65-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="33b65-110">PARAMETERS</span></span>

### <span data-ttu-id="33b65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33b65-111">-DefaultProfile</span></span>
<span data-ttu-id="33b65-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33b65-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33b65-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="33b65-113">-Name</span></span>
<span data-ttu-id="33b65-114">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="33b65-114">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b65-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33b65-115">-ResourceGroupName</span></span>
<span data-ttu-id="33b65-116">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="33b65-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b65-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b65-117">CommonParameters</span></span>
<span data-ttu-id="33b65-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="33b65-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b65-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33b65-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b65-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="33b65-120">INPUTS</span></span>

### <span data-ttu-id="33b65-121">System. String</span><span class="sxs-lookup"><span data-stu-id="33b65-121">System.String</span></span>

## <span data-ttu-id="33b65-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33b65-122">OUTPUTS</span></span>

### <span data-ttu-id="33b65-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="33b65-123">System.Boolean</span></span>

## <span data-ttu-id="33b65-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="33b65-124">NOTES</span></span>
<span data-ttu-id="33b65-125">Alias (псевдоним): Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="33b65-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="33b65-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33b65-126">RELATED LINKS</span></span>

[<span data-ttu-id="33b65-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="33b65-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="33b65-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="33b65-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
