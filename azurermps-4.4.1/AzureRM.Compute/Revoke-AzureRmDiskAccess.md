---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: 58cbbfd2314589fd6b28f2ff375aa268c39e63d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557847"
---
# <span data-ttu-id="8a6b0-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8a6b0-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="8a6b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a6b0-102">SYNOPSIS</span></span>
<span data-ttu-id="8a6b0-103">Отменяет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="8a6b0-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a6b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a6b0-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a6b0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a6b0-105">DESCRIPTION</span></span>
<span data-ttu-id="8a6b0-106">Командлет **REVOKE-AzureRmDiskAccess** отменяет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="8a6b0-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="8a6b0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a6b0-107">EXAMPLES</span></span>

### <span data-ttu-id="8a6b0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8a6b0-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="8a6b0-109">Отмена доступа к диску с именем "Disk01" в группе ресурсов с именем "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="8a6b0-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="8a6b0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a6b0-110">PARAMETERS</span></span>

### <span data-ttu-id="8a6b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a6b0-111">-DefaultProfile</span></span>
<span data-ttu-id="8a6b0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a6b0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a6b0-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="8a6b0-113">-DiskName</span></span>
<span data-ttu-id="8a6b0-114">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="8a6b0-114">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="8a6b0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a6b0-115">-ResourceGroupName</span></span>
<span data-ttu-id="8a6b0-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a6b0-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8a6b0-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a6b0-117">-Confirm</span></span>
<span data-ttu-id="8a6b0-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8a6b0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a6b0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a6b0-119">-WhatIf</span></span>
<span data-ttu-id="8a6b0-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8a6b0-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a6b0-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8a6b0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a6b0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a6b0-122">CommonParameters</span></span>
<span data-ttu-id="8a6b0-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a6b0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a6b0-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a6b0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a6b0-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a6b0-125">INPUTS</span></span>

### <span data-ttu-id="8a6b0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8a6b0-126">System.String</span></span>

## <span data-ttu-id="8a6b0-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a6b0-127">OUTPUTS</span></span>

### <span data-ttu-id="8a6b0-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="8a6b0-128">System.Object</span></span>

## <span data-ttu-id="8a6b0-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a6b0-129">NOTES</span></span>

## <span data-ttu-id="8a6b0-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a6b0-130">RELATED LINKS</span></span>

