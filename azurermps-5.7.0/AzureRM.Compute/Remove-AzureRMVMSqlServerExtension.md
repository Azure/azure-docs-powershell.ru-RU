---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: f074d61919098d6c23ab39424774d9ba18e457d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559176"
---
# <span data-ttu-id="b7933-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b7933-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="b7933-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7933-102">SYNOPSIS</span></span>
<span data-ttu-id="b7933-103">Удаляет расширение SQL Server из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b7933-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7933-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7933-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="b7933-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7933-105">DESCRIPTION</span></span>
<span data-ttu-id="b7933-106">Командлет **Remove-AzureRmVMSqlServerExtension** удаляет расширение сервера AzureSQL из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b7933-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="b7933-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7933-107">EXAMPLES</span></span>

### <span data-ttu-id="b7933-108">Пример 1: удаление расширения SQL Server</span><span class="sxs-lookup"><span data-stu-id="b7933-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="b7933-109">Эта команда удаляет расширение SQL Server из виртуальной машины с именем ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="b7933-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="b7933-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7933-110">PARAMETERS</span></span>

### <span data-ttu-id="b7933-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7933-111">-Name</span></span>
<span data-ttu-id="b7933-112">Указывает имя сервера SQL Server, расширение которого удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b7933-112">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7933-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7933-113">-ResourceGroupName</span></span>
<span data-ttu-id="b7933-114">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b7933-114">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7933-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="b7933-115">-VMName</span></span>
<span data-ttu-id="b7933-116">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b7933-116">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7933-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7933-117">CommonParameters</span></span>
<span data-ttu-id="b7933-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7933-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7933-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7933-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7933-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7933-120">INPUTS</span></span>

### <span data-ttu-id="b7933-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="b7933-121">None</span></span>
<span data-ttu-id="b7933-122">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b7933-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b7933-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7933-123">OUTPUTS</span></span>

## <span data-ttu-id="b7933-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7933-124">NOTES</span></span>

## <span data-ttu-id="b7933-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7933-125">RELATED LINKS</span></span>

[<span data-ttu-id="b7933-126">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b7933-126">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="b7933-127">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b7933-127">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


