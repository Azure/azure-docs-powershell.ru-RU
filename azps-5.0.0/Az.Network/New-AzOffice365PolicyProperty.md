---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9fae8c6d543bddc3ad4110b95a1c1b4a1f146879
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317105"
---
# <span data-ttu-id="8b0ce-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="8b0ce-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="8b0ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b0ce-102">SYNOPSIS</span></span>
<span data-ttu-id="8b0ce-103">Определение новой политики трафика Office 365 для использования с сайтом виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="8b0ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b0ce-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b0ce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b0ce-105">DESCRIPTION</span></span>
<span data-ttu-id="8b0ce-106">Команда New-AzOffice365PolicyProperties определяет политику помещения Office 365, которая будет использоваться на сайте виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used with a Virtual Appliance site.</span></span> 

## <span data-ttu-id="8b0ce-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b0ce-107">EXAMPLES</span></span>

### <span data-ttu-id="8b0ce-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b0ce-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="8b0ce-109">Создание объекта политики трафика Office 365 для использования с командами сайта виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="8b0ce-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b0ce-110">PARAMETERS</span></span>

### <span data-ttu-id="8b0ce-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="8b0ce-111">-Allow</span></span>
<span data-ttu-id="8b0ce-112">Выступающий трафик категории Allowed.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="8b0ce-113">-Default</span><span class="sxs-lookup"><span data-stu-id="8b0ce-113">-Default</span></span>
<span data-ttu-id="8b0ce-114">Изменяйте трафик по категориям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="8b0ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b0ce-115">-DefaultProfile</span></span>
<span data-ttu-id="8b0ce-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b0ce-117">-OPTIMIZE</span><span class="sxs-lookup"><span data-stu-id="8b0ce-117">-Optimize</span></span>
<span data-ttu-id="8b0ce-118">Выступающий трафик оптимизации категории.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="8b0ce-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b0ce-119">CommonParameters</span></span>
<span data-ttu-id="8b0ce-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b0ce-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b0ce-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b0ce-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b0ce-122">INPUTS</span></span>

### <span data-ttu-id="8b0ce-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="8b0ce-123">None</span></span>

## <span data-ttu-id="8b0ce-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b0ce-124">OUTPUTS</span></span>

### <span data-ttu-id="8b0ce-125">Microsoft. Azure. Commands. Network. Models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="8b0ce-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="8b0ce-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b0ce-126">NOTES</span></span>

## <span data-ttu-id="8b0ce-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b0ce-127">RELATED LINKS</span></span>
