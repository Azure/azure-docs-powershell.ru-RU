---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
ms.openlocfilehash: e75c34d76c304af272655c3e4e81fcfd547d11b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567141"
---
# <span data-ttu-id="234f9-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="234f9-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="234f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="234f9-102">SYNOPSIS</span></span>
<span data-ttu-id="234f9-103">Удаляет расширение AEM из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="234f9-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="234f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="234f9-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="234f9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="234f9-105">DESCRIPTION</span></span>
<span data-ttu-id="234f9-106">Командлет **Remove-AzureRmVMAEMExtension** удаляет расширение службы улучшенного мониторинга Azure (AEM) с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="234f9-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="234f9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="234f9-107">EXAMPLES</span></span>

### <span data-ttu-id="234f9-108">Пример 1: удаление расширения AEM</span><span class="sxs-lookup"><span data-stu-id="234f9-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="234f9-109">Эта команда удаляет расширение AEM для виртуальной машины с именем Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="234f9-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="234f9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="234f9-110">PARAMETERS</span></span>

### <span data-ttu-id="234f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="234f9-111">-DefaultProfile</span></span>
<span data-ttu-id="234f9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="234f9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="234f9-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="234f9-113">-Name</span></span>
<span data-ttu-id="234f9-114">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение AEM.</span><span class="sxs-lookup"><span data-stu-id="234f9-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="234f9-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="234f9-115">-OSType</span></span>
<span data-ttu-id="234f9-116">Указывает тип операционной системы диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="234f9-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="234f9-117">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="234f9-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="234f9-118">Допустимые значения этого параметра: Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="234f9-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="234f9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="234f9-119">-ResourceGroupName</span></span>
<span data-ttu-id="234f9-120">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="234f9-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="234f9-121">Этот командлет удаляет расширение AEM из этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="234f9-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="234f9-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="234f9-122">-VMName</span></span>
<span data-ttu-id="234f9-123">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="234f9-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="234f9-124">Этот командлет удаляет расширение AEM для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="234f9-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="234f9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="234f9-125">CommonParameters</span></span>
<span data-ttu-id="234f9-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="234f9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="234f9-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="234f9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="234f9-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="234f9-128">INPUTS</span></span>

## <span data-ttu-id="234f9-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="234f9-129">OUTPUTS</span></span>

## <span data-ttu-id="234f9-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="234f9-130">NOTES</span></span>

## <span data-ttu-id="234f9-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="234f9-131">RELATED LINKS</span></span>

[<span data-ttu-id="234f9-132">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="234f9-132">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="234f9-133">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="234f9-133">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="234f9-134">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="234f9-134">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


