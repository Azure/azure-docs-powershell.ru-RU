---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
ms.openlocfilehash: fd52bf58e3e240f65be88d8f9f682b2543e1f458
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735195"
---
# <span data-ttu-id="b7aec-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="b7aec-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="b7aec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7aec-102">SYNOPSIS</span></span>
<span data-ttu-id="b7aec-103">Открыть командный документ.</span><span class="sxs-lookup"><span data-stu-id="b7aec-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7aec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7aec-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7aec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7aec-105">DESCRIPTION</span></span>
<span data-ttu-id="b7aec-106">Открыть командный документ.</span><span class="sxs-lookup"><span data-stu-id="b7aec-106">Get run command document.</span></span>

## <span data-ttu-id="b7aec-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7aec-107">EXAMPLES</span></span>

### <span data-ttu-id="b7aec-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b7aec-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="b7aec-109">Возвращает определенный документ команды запуска для "RunPowerShellScript" в "westus".</span><span class="sxs-lookup"><span data-stu-id="b7aec-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="b7aec-110">$Loc расположения Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="b7aec-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="b7aec-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b7aec-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="b7aec-112">Список всех доступных команд выполнения в "westus".</span><span class="sxs-lookup"><span data-stu-id="b7aec-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="b7aec-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7aec-113">PARAMETERS</span></span>

### <span data-ttu-id="b7aec-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="b7aec-114">-CommandId</span></span>
<span data-ttu-id="b7aec-115">Идентификатор команды.</span><span class="sxs-lookup"><span data-stu-id="b7aec-115">The command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7aec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7aec-116">-DefaultProfile</span></span>
<span data-ttu-id="b7aec-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7aec-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7aec-118">-Location</span><span class="sxs-lookup"><span data-stu-id="b7aec-118">-Location</span></span>
<span data-ttu-id="b7aec-119">Расположение, в котором запрашиваются команды выполнения.</span><span class="sxs-lookup"><span data-stu-id="b7aec-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="b7aec-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7aec-120">CommonParameters</span></span>
<span data-ttu-id="b7aec-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7aec-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7aec-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7aec-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7aec-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7aec-123">INPUTS</span></span>

### <span data-ttu-id="b7aec-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b7aec-124">System.String</span></span>

## <span data-ttu-id="b7aec-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7aec-125">OUTPUTS</span></span>

### <span data-ttu-id="b7aec-126">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="b7aec-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="b7aec-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7aec-127">NOTES</span></span>

## <span data-ttu-id="b7aec-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7aec-128">RELATED LINKS</span></span>

