---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 8e5041b57c4063a3d1ceb2f62e0149132c21b953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567198"
---
# <span data-ttu-id="61ced-101">Test-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="61ced-101">Test-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="61ced-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61ced-102">SYNOPSIS</span></span>
<span data-ttu-id="61ced-103">Проверка существования экземпляра сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="61ced-103">Tests the existence of an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61ced-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61ced-104">SYNTAX</span></span>

```
Test-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61ced-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61ced-105">DESCRIPTION</span></span>
<span data-ttu-id="61ced-106">Командлет Test-AzureRmAnalysisServicesServer проверяет наличие экземпляра сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="61ced-106">The Test-AzureRmAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="61ced-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61ced-107">EXAMPLES</span></span>

### <span data-ttu-id="61ced-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="61ced-108">Example 1</span></span>
```
PS C:\> Test-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="61ced-109">Эта команда пройдет проверку на наличие сервера с именем TestServer в группе resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="61ced-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="61ced-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61ced-110">PARAMETERS</span></span>

### <span data-ttu-id="61ced-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="61ced-111">-Name</span></span>
<span data-ttu-id="61ced-112">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="61ced-112">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="61ced-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61ced-113">-ResourceGroupName</span></span>
<span data-ttu-id="61ced-114">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="61ced-114">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="61ced-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ced-115">-DefaultProfile</span></span>
<span data-ttu-id="61ced-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61ced-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61ced-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ced-117">CommonParameters</span></span>
<span data-ttu-id="61ced-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61ced-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ced-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61ced-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ced-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61ced-120">INPUTS</span></span>

## <span data-ttu-id="61ced-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61ced-121">OUTPUTS</span></span>

### <span data-ttu-id="61ced-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="61ced-122">System.Boolean</span></span>

## <span data-ttu-id="61ced-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="61ced-123">NOTES</span></span>
<span data-ttu-id="61ced-124">Alias (псевдоним): Test-AzureAs</span><span class="sxs-lookup"><span data-stu-id="61ced-124">Alias: Test-AzureAs</span></span>

## <span data-ttu-id="61ced-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61ced-125">RELATED LINKS</span></span>

[<span data-ttu-id="61ced-126">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="61ced-126">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="61ced-127">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="61ced-127">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
