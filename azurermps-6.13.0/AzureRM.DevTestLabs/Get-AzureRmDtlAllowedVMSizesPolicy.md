---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: db82ca43114a35921652424289fcc53f7761ab8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563079"
---
# <span data-ttu-id="72259-101">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="72259-101">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="72259-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72259-102">SYNOPSIS</span></span>
<span data-ttu-id="72259-103">Получение политики размеров разрешенных виртуальных машин для лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="72259-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72259-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72259-104">SYNTAX</span></span>

```
Get-AzureRmDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72259-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72259-105">DESCRIPTION</span></span>
<span data-ttu-id="72259-106">Командлет **Get-AzureRmDtlAllowedVMSizesPolicy** получает политику допустимых размеров виртуальных машин, которая позволяет указать список допустимых размеров виртуальных машин в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="72259-106">The **Get-AzureRmDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="72259-107">Командлет возвращает состояние включения или отключения политики и список всех допустимых размеров виртуальных машин, заданных в указанной политике.</span><span class="sxs-lookup"><span data-stu-id="72259-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="72259-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72259-108">EXAMPLES</span></span>

## <span data-ttu-id="72259-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72259-109">PARAMETERS</span></span>

### <span data-ttu-id="72259-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72259-110">-DefaultProfile</span></span>
<span data-ttu-id="72259-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="72259-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72259-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="72259-112">-LabName</span></span>
<span data-ttu-id="72259-113">Указывает имя лаборатории, для которой этот командлет получает политику размера виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="72259-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="72259-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72259-114">-ResourceGroupName</span></span>
<span data-ttu-id="72259-115">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="72259-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72259-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72259-116">CommonParameters</span></span>
<span data-ttu-id="72259-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72259-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72259-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72259-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72259-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72259-119">INPUTS</span></span>

### <span data-ttu-id="72259-120">System. String</span><span class="sxs-lookup"><span data-stu-id="72259-120">System.String</span></span>

## <span data-ttu-id="72259-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72259-121">OUTPUTS</span></span>

### <span data-ttu-id="72259-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="72259-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="72259-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="72259-123">NOTES</span></span>

## <span data-ttu-id="72259-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72259-124">RELATED LINKS</span></span>

[<span data-ttu-id="72259-125">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="72259-125">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Set-AzureRmDtlAllowedVMSizesPolicy.md)

[<span data-ttu-id="72259-126">Командлеты лаборатории тестирования для разработчиков Azure</span><span class="sxs-lookup"><span data-stu-id="72259-126">Azure Development Test Lab Cmdlets</span></span>](./AzureRM.DevTestLabs.md)


