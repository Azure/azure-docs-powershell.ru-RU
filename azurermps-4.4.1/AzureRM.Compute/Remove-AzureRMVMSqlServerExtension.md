---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: 19d4022fcf5f3eee0ee8d77e7c061ae2f8d00629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568805"
---
# <span data-ttu-id="18bba-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="18bba-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="18bba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="18bba-102">SYNOPSIS</span></span>
<span data-ttu-id="18bba-103">Удаляет расширение SQL Server из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="18bba-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18bba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="18bba-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18bba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18bba-105">DESCRIPTION</span></span>
<span data-ttu-id="18bba-106">Командлет **Remove-AzureRmVMSqlServerExtension** удаляет расширение сервера AzureSQL из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="18bba-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="18bba-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="18bba-107">EXAMPLES</span></span>

### <span data-ttu-id="18bba-108">Пример 1: удаление расширения SQL Server</span><span class="sxs-lookup"><span data-stu-id="18bba-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="18bba-109">Эта команда удаляет расширение SQL Server из виртуальной машины с именем ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="18bba-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="18bba-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="18bba-110">PARAMETERS</span></span>

### <span data-ttu-id="18bba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18bba-111">-DefaultProfile</span></span>
<span data-ttu-id="18bba-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18bba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18bba-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="18bba-113">-Name</span></span>
<span data-ttu-id="18bba-114">Указывает имя сервера SQL Server, расширение которого удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="18bba-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="18bba-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18bba-115">-ResourceGroupName</span></span>
<span data-ttu-id="18bba-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="18bba-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="18bba-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="18bba-117">-VMName</span></span>
<span data-ttu-id="18bba-118">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение SQL Server.</span><span class="sxs-lookup"><span data-stu-id="18bba-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="18bba-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18bba-119">CommonParameters</span></span>
<span data-ttu-id="18bba-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="18bba-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18bba-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18bba-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18bba-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="18bba-122">INPUTS</span></span>

## <span data-ttu-id="18bba-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="18bba-123">OUTPUTS</span></span>

## <span data-ttu-id="18bba-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="18bba-124">NOTES</span></span>

## <span data-ttu-id="18bba-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18bba-125">RELATED LINKS</span></span>

[<span data-ttu-id="18bba-126">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="18bba-126">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="18bba-127">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="18bba-127">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


