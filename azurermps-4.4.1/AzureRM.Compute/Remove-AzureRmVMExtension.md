---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
ms.openlocfilehash: 164fdd36ca0e97dde33caec1322ddfa2bb6a15c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557879"
---
# <span data-ttu-id="67937-101">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="67937-101">Remove-AzureRmVMExtension</span></span>

## <span data-ttu-id="67937-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67937-102">SYNOPSIS</span></span>
<span data-ttu-id="67937-103">Удаляет расширение из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="67937-103">Removes an extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67937-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67937-104">SYNTAX</span></span>

```
Remove-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67937-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67937-105">DESCRIPTION</span></span>
<span data-ttu-id="67937-106">Командлет **Remove-AzureRmVMExtension** удаляет расширение из расширений виртуальных машин виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="67937-106">The **Remove-AzureRmVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="67937-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67937-107">EXAMPLES</span></span>

### <span data-ttu-id="67937-108">Пример 1: удаление расширения из виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="67937-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="67937-109">Эта команда удаляет расширение ContosoTest с виртуальной машины с именем VirtualMachine22 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="67937-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="67937-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67937-110">PARAMETERS</span></span>

### <span data-ttu-id="67937-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67937-111">-DefaultProfile</span></span>
<span data-ttu-id="67937-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67937-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67937-113">-Force</span><span class="sxs-lookup"><span data-stu-id="67937-113">-Force</span></span>
<span data-ttu-id="67937-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="67937-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="67937-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="67937-115">-Name</span></span>
<span data-ttu-id="67937-116">Указывает имя расширения, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="67937-116">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67937-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67937-117">-ResourceGroupName</span></span>
<span data-ttu-id="67937-118">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="67937-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="67937-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="67937-119">-VMName</span></span>
<span data-ttu-id="67937-120">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение.</span><span class="sxs-lookup"><span data-stu-id="67937-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67937-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67937-121">-Confirm</span></span>
<span data-ttu-id="67937-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="67937-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67937-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67937-123">-WhatIf</span></span>
<span data-ttu-id="67937-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="67937-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="67937-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="67937-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67937-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67937-126">CommonParameters</span></span>
<span data-ttu-id="67937-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67937-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67937-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67937-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67937-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67937-129">INPUTS</span></span>

## <span data-ttu-id="67937-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67937-130">OUTPUTS</span></span>

## <span data-ttu-id="67937-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="67937-131">NOTES</span></span>

## <span data-ttu-id="67937-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67937-132">RELATED LINKS</span></span>

[<span data-ttu-id="67937-133">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="67937-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="67937-134">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="67937-134">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


