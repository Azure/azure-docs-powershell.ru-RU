---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: bcfba4bb002d7982f9a0fb9220fbce24e12e6ffb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569615"
---
# <span data-ttu-id="3c663-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="3c663-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="3c663-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c663-102">SYNOPSIS</span></span>
<span data-ttu-id="3c663-103">Удаление диска.</span><span class="sxs-lookup"><span data-stu-id="3c663-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c663-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c663-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c663-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c663-105">DESCRIPTION</span></span>
<span data-ttu-id="3c663-106">Командлет **Remove-AzureRmDisk** удаляет диск.</span><span class="sxs-lookup"><span data-stu-id="3c663-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="3c663-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c663-107">EXAMPLES</span></span>

### <span data-ttu-id="3c663-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3c663-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="3c663-109">Эта команда удаляет диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3c663-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3c663-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c663-110">PARAMETERS</span></span>

### <span data-ttu-id="3c663-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c663-111">-DefaultProfile</span></span>
<span data-ttu-id="3c663-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c663-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c663-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="3c663-113">-DiskName</span></span>
<span data-ttu-id="3c663-114">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="3c663-114">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c663-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3c663-115">-Force</span></span>
<span data-ttu-id="3c663-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3c663-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c663-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c663-117">-ResourceGroupName</span></span>
<span data-ttu-id="3c663-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3c663-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3c663-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c663-119">-Confirm</span></span>
<span data-ttu-id="3c663-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3c663-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c663-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c663-121">-WhatIf</span></span>
<span data-ttu-id="3c663-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3c663-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c663-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3c663-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c663-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c663-124">CommonParameters</span></span>
<span data-ttu-id="3c663-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c663-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c663-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c663-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c663-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c663-127">INPUTS</span></span>

### <span data-ttu-id="3c663-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3c663-128">System.String</span></span>

## <span data-ttu-id="3c663-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c663-129">OUTPUTS</span></span>

### <span data-ttu-id="3c663-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="3c663-130">System.Object</span></span>

## <span data-ttu-id="3c663-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c663-131">NOTES</span></span>

## <span data-ttu-id="3c663-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c663-132">RELATED LINKS</span></span>

