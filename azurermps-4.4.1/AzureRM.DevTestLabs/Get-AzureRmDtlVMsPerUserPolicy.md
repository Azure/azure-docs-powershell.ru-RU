---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 2be26f222be7ec444706fb15fb862a43dc8b8116
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567648"
---
# <span data-ttu-id="af1b0-101">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="af1b0-101">Get-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="af1b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af1b0-102">SYNOPSIS</span></span>
<span data-ttu-id="af1b0-103">Возвращает политику виртуальных машин на пользователя лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="af1b0-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af1b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af1b0-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af1b0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af1b0-105">DESCRIPTION</span></span>
<span data-ttu-id="af1b0-106">Командлет **Get-AzureRmDtlVMsPerUserPolicy** получает виртуальные машины для пользовательской политики лаборатории, которая позволяет установить максимальное количество виртуальных машин, разрешенных для одного пользователя.</span><span class="sxs-lookup"><span data-stu-id="af1b0-106">The **Get-AzureRmDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="af1b0-107">Командлет возвращает состояние политики "включено" или "отключено", а также максимальное количество виртуальных машин, разрешенных для одного пользователя, установленного в политике.</span><span class="sxs-lookup"><span data-stu-id="af1b0-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="af1b0-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af1b0-108">EXAMPLES</span></span>

## <span data-ttu-id="af1b0-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af1b0-109">PARAMETERS</span></span>

### <span data-ttu-id="af1b0-110">-LabName</span><span class="sxs-lookup"><span data-stu-id="af1b0-110">-LabName</span></span>
<span data-ttu-id="af1b0-111">Указывает имя лаборатории, для которой этот командлет получает политику виртуальной машины на пользователя.</span><span class="sxs-lookup"><span data-stu-id="af1b0-111">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="af1b0-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af1b0-112">-ResourceGroupName</span></span>
<span data-ttu-id="af1b0-113">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="af1b0-113">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="af1b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af1b0-114">-DefaultProfile</span></span>
<span data-ttu-id="af1b0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af1b0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af1b0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af1b0-116">CommonParameters</span></span>
<span data-ttu-id="af1b0-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af1b0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af1b0-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af1b0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af1b0-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af1b0-119">INPUTS</span></span>

## <span data-ttu-id="af1b0-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af1b0-120">OUTPUTS</span></span>

### <span data-ttu-id="af1b0-121">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="af1b0-121">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="af1b0-122">Этот командлет возвращает политику, указывающую максимальное количество виртуальных машин, которые могут быть созданы пользователем в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="af1b0-122">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="af1b0-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="af1b0-123">NOTES</span></span>

## <span data-ttu-id="af1b0-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af1b0-124">RELATED LINKS</span></span>

[<span data-ttu-id="af1b0-125">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="af1b0-125">Set-AzureRmDtlVMsPerUserPolicy</span></span>](./Set-AzureRmDtlVMsPerUserPolicy.md)


