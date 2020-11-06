---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 4e252001d1459c52a35b766d34c91050df62073d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563691"
---
# <span data-ttu-id="03a98-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="03a98-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="03a98-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03a98-102">SYNOPSIS</span></span>
<span data-ttu-id="03a98-103">Создает объект конфигурации для учетных данных хранилища ключей SQL Server на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="03a98-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03a98-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03a98-104">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03a98-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03a98-105">DESCRIPTION</span></span>

## <span data-ttu-id="03a98-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03a98-106">EXAMPLES</span></span>

## <span data-ttu-id="03a98-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03a98-107">PARAMETERS</span></span>

### <span data-ttu-id="03a98-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="03a98-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a98-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="03a98-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a98-110">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="03a98-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a98-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03a98-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="03a98-112">-Намерено</span><span class="sxs-lookup"><span data-stu-id="03a98-112">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a98-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="03a98-113">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a98-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03a98-114">-Confirm</span></span>
<span data-ttu-id="03a98-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="03a98-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a98-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03a98-116">-WhatIf</span></span>
<span data-ttu-id="03a98-117">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="03a98-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="03a98-118">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="03a98-118">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a98-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a98-119">CommonParameters</span></span>
<span data-ttu-id="03a98-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="03a98-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a98-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03a98-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a98-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03a98-122">INPUTS</span></span>

### <span data-ttu-id="03a98-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="03a98-123">None</span></span>
<span data-ttu-id="03a98-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="03a98-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="03a98-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03a98-125">OUTPUTS</span></span>

## <span data-ttu-id="03a98-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="03a98-126">NOTES</span></span>

## <span data-ttu-id="03a98-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03a98-127">RELATED LINKS</span></span>

