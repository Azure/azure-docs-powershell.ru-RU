---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: a1b06a870822f2fef0bf2f9a39321c13642f8cad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570103"
---
# <span data-ttu-id="0d8e4-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="0d8e4-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="0d8e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d8e4-102">SYNOPSIS</span></span>
<span data-ttu-id="0d8e4-103">Предоставление доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d8e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d8e4-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d8e4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d8e4-105">DESCRIPTION</span></span>
<span data-ttu-id="0d8e4-106">Командлет **Grant-AzureRmDiskAccess** предоставляет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="0d8e4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d8e4-107">EXAMPLES</span></span>

### <span data-ttu-id="0d8e4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0d8e4-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="0d8e4-109">Предоставление доступа для чтения к диску с именем "Disk01" в группе ресурсов с именем "ResourceGroup01" для 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="0d8e4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d8e4-110">PARAMETERS</span></span>

### <span data-ttu-id="0d8e4-111">-Доступ</span><span class="sxs-lookup"><span data-stu-id="0d8e4-111">-Access</span></span>
<span data-ttu-id="0d8e4-112">Определяет уровень доступа.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-112">Specifies Access level.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d8e4-113">-DefaultProfile</span></span>
<span data-ttu-id="0d8e4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d8e4-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="0d8e4-115">-DiskName</span></span>
<span data-ttu-id="0d8e4-116">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="0d8e4-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="0d8e4-117">-DurationInSecond</span></span>
<span data-ttu-id="0d8e4-118">Указывает продолжительность доступа в секундах.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8e4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d8e4-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d8e4-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0d8e4-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d8e4-121">-Confirm</span></span>
<span data-ttu-id="0d8e4-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d8e4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d8e4-123">-WhatIf</span></span>
<span data-ttu-id="0d8e4-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d8e4-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d8e4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d8e4-126">CommonParameters</span></span>
<span data-ttu-id="0d8e4-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d8e4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d8e4-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d8e4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d8e4-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d8e4-129">INPUTS</span></span>

### <span data-ttu-id="0d8e4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0d8e4-130">System.String</span></span>

## <span data-ttu-id="0d8e4-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d8e4-131">OUTPUTS</span></span>

### <span data-ttu-id="0d8e4-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="0d8e4-132">System.Object</span></span>

## <span data-ttu-id="0d8e4-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d8e4-133">NOTES</span></span>

## <span data-ttu-id="0d8e4-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d8e4-134">RELATED LINKS</span></span>

