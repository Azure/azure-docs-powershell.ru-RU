---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: 5d99bafdd011409eae322c60db6e596d3c77cd4f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910245"
---
# <span data-ttu-id="6c1bc-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="6c1bc-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="6c1bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6c1bc-102">SYNOPSIS</span></span>
<span data-ttu-id="6c1bc-103">Получает профиль журнала.</span><span class="sxs-lookup"><span data-stu-id="6c1bc-103">Gets a log profile.</span></span>

## <span data-ttu-id="6c1bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6c1bc-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c1bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c1bc-105">DESCRIPTION</span></span>
<span data-ttu-id="6c1bc-106">Командлет **Get-AzLogProfile** получает профиль журнала.</span><span class="sxs-lookup"><span data-stu-id="6c1bc-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="6c1bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6c1bc-107">EXAMPLES</span></span>

## <span data-ttu-id="6c1bc-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6c1bc-108">PARAMETERS</span></span>

### <span data-ttu-id="6c1bc-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c1bc-109">-DefaultProfile</span></span>
<span data-ttu-id="6c1bc-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6c1bc-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c1bc-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6c1bc-111">-Name</span></span>
<span data-ttu-id="6c1bc-112">Указывает имя профиля, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="6c1bc-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c1bc-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c1bc-113">CommonParameters</span></span>
<span data-ttu-id="6c1bc-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6c1bc-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c1bc-115">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c1bc-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c1bc-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6c1bc-116">INPUTS</span></span>

### <span data-ttu-id="6c1bc-117">System. String</span><span class="sxs-lookup"><span data-stu-id="6c1bc-117">System.String</span></span>

## <span data-ttu-id="6c1bc-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c1bc-118">OUTPUTS</span></span>

### <span data-ttu-id="6c1bc-119">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="6c1bc-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="6c1bc-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="6c1bc-120">NOTES</span></span>

## <span data-ttu-id="6c1bc-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c1bc-121">RELATED LINKS</span></span>

[<span data-ttu-id="6c1bc-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="6c1bc-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="6c1bc-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="6c1bc-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


