---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7EB9FE4-BDEB-43A5-B6D3-FEAB16BC2711
online version: ''
schema: 2.0.0
ms.openlocfilehash: 388277115281cbbacfb634ebdac5cdd9aa86b709
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077414"
---
# <span data-ttu-id="1f7cb-101">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="1f7cb-101">Get-WAPackVMRole</span></span>

## <span data-ttu-id="1f7cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f7cb-102">SYNOPSIS</span></span>

## <span data-ttu-id="1f7cb-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f7cb-103">SYNTAX</span></span>

### <span data-ttu-id="1f7cb-104">Пустой (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1f7cb-104">Empty (Default)</span></span>
```
Get-WAPackVMRole [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1f7cb-105">FromName</span><span class="sxs-lookup"><span data-stu-id="1f7cb-105">FromName</span></span>
```
Get-WAPackVMRole -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1f7cb-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="1f7cb-106">FromCloudService</span></span>
```
Get-WAPackVMRole -Name <String> -CloudServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1f7cb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f7cb-107">DESCRIPTION</span></span>
<span data-ttu-id="1f7cb-108">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="1f7cb-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="1f7cb-109">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1f7cb-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1f7cb-110">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1f7cb-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="1f7cb-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f7cb-111">EXAMPLES</span></span>

### <span data-ttu-id="1f7cb-112">Пример 1: получение роли виртуальной машины (созданной на портале)</span><span class="sxs-lookup"><span data-stu-id="1f7cb-112">Example 1: Get a virtual machine role (created through the portal)</span></span>
```
PS C:\> Get-WAPackVMRole -Name "ContosoVMRole01"
```

<span data-ttu-id="1f7cb-113">Эта команда получает роль виртуальной машины, созданную с помощью портала с именем ContosoVMRole01.</span><span class="sxs-lookup"><span data-stu-id="1f7cb-113">This command gets a virtual machine role which has been created through the portal named ContosoVMRole01.</span></span>

### <span data-ttu-id="1f7cb-114">Пример 2: получение роли виртуальной машины с помощью имени и имени облачной службы</span><span class="sxs-lookup"><span data-stu-id="1f7cb-114">Example 2: Get a virtual machine role by using a name and a cloud service name</span></span>
```
PS C:\> Get-WAPackVMRole -CloudServiceName "ContosoCloudService01" -Name "ContosoVMRole02"
```

<span data-ttu-id="1f7cb-115">Эта команда получает роль виртуальной машины с именем ContosoVMRole02, которая находится в облачной службе с именем ContosoCloudService01.</span><span class="sxs-lookup"><span data-stu-id="1f7cb-115">This command gets a virtual machine role named ContosoVMRole02 which stand on a cloud service named ContosoCloudService01.</span></span>

### <span data-ttu-id="1f7cb-116">Пример 3: получение всей роли виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="1f7cb-116">Example 3: Get all virtual machine role</span></span>
```
PS C:\> Get-WAPackVMRole
```

<span data-ttu-id="1f7cb-117">Эта команда получает все существующие роли виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1f7cb-117">This command gets all existing virtual machine role.</span></span>

## <span data-ttu-id="1f7cb-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f7cb-118">PARAMETERS</span></span>

### <span data-ttu-id="1f7cb-119">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="1f7cb-119">-CloudServiceName</span></span>
<span data-ttu-id="1f7cb-120">Указывает имя облачной службы для роли виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1f7cb-120">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f7cb-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1f7cb-121">-Name</span></span>
<span data-ttu-id="1f7cb-122">Указывает имя роли виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1f7cb-122">Specifies the name of a virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromName, FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f7cb-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="1f7cb-123">-Profile</span></span>
<span data-ttu-id="1f7cb-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1f7cb-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1f7cb-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1f7cb-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7cb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f7cb-126">CommonParameters</span></span>
<span data-ttu-id="1f7cb-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f7cb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f7cb-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f7cb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f7cb-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f7cb-129">INPUTS</span></span>

## <span data-ttu-id="1f7cb-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f7cb-130">OUTPUTS</span></span>

## <span data-ttu-id="1f7cb-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f7cb-131">NOTES</span></span>

## <span data-ttu-id="1f7cb-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f7cb-132">RELATED LINKS</span></span>

[<span data-ttu-id="1f7cb-133">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="1f7cb-133">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="1f7cb-134">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="1f7cb-134">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="1f7cb-135">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="1f7cb-135">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


